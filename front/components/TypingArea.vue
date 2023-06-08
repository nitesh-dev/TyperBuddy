<script setup lang='ts'>

interface TyperData {
    class: string,
    text: string
}

interface CursorPos {
    row: number,
    col: number
}



const cursor = ref<HTMLSpanElement>()
const typingTextarea = ref<HTMLTextAreaElement>()

onMounted(function () {
    setupData()

    if (typingTextarea == undefined) return
    typingTextarea.value!!.addEventListener('mousedown', function (event) {

        this.focus()
        event.preventDefault();
    });

    typingTextarea.value!!.addEventListener('copy', function (event) {
        event.preventDefault();
    });

    typingTextarea.value!!.addEventListener('paste', function (event) {
        event.preventDefault();
    });

})


function setupData() {
    manipulateText('')
}



var dataContent = "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged."
const allWords = ref(Array<TyperData>())


function manipulateText(text: string) {
    if (typingTextarea == undefined) return

    allWords.value = Array<TyperData>()
    // parsing text
    var successText = ''
    var errorText = ''
    const totalChar = Math.min(text.length, dataContent.length)

    for (let index = 0; index < totalChar; index++) {
        let charAt = dataContent[index]

        // handle correct text
        if (charAt == text[index]) {

            // adding error text if not empty
            if (errorText != '') {
                allWords.value.push({
                    class: 'error',
                    text: errorText
                })

                errorText = ''
            }

            successText += charAt
        } else {

            // adding success text if not empty
            if (successText != '') {
                allWords.value.push({
                    class: 'success',
                    text: successText
                })

                successText = ''
            }

            errorText += charAt
        }
    }


    // adding any left text
    if (errorText != '') {
        allWords.value.push({
            class: 'error',
            text: errorText
        })
    }

    if (successText != '') {
        allWords.value.push({
            class: 'success',
            text: successText
        })
    }


    // extracting the not typed text
    if (dataContent.length > text.length) {

        let normalText = ''
        let caretText = dataContent[totalChar]
        if ((dataContent.length - text.length) > 1) {
            normalText = dataContent.slice(totalChar + 1)
        }

        allWords.value.push({
            class: 'caret',
            text: caretText
        })

        if (normalText != '') {
            allWords.value.push({
                class: 'normal',
                text: normalText
            })
        }

    }

}



</script>
<template>
    <div class="typing-content">
        <div class="content-holder">
            <span ref="cursor" class="cursor"></span>

            <div class="content">
                <span v-for="word in allWords" :class="word.class">{{ word.text }}</span>
            </div>

            <textarea ref="typingTextarea" id="typing-textarea"
                @input="event => manipulateText((event.target as any).value)"></textarea>

        </div>
    </div>
</template>
<style scoped>
/* -------------------- Typing content ------------------- */
.typing-content {
    width: 100%;
    max-width: 800px;
    margin: auto;
    background-color: white;
    border-radius: 0.6rem;
    color: var(--color-on-surface);
    line-height: 1.8;
    padding: 1rem 1.6rem;
    font-size: var(--big-2-font);
}

.typing-content .success {
    color: var(--color-on-surface);
}

.typing-content .error {
    color: var(--color-on-error);
    background-color: var(--color-error);
}

.typing-content .normal {
    opacity: 0.75;
}

.typing-content span {
    font-family: monospace !important;
    letter-spacing: 3px;
}

.typing-content .content-holder {
    position: relative;
}


.typing-content .caret {
    background-color: var(--color-on-surface);
    color: white;
}

.typing-content .cursor {
    position: absolute;
    top: 6px;
    left: 0;
    width: 3px;
    height: 2.5rem;
    background-color: var(--color-secondary);
    display: none;
}

.typing-content .content {
    height: 300px;
    overflow: hidden;
}

.typing-content textarea {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    outline: none;
    border: none;
    opacity: 0;
    font-family: monospace !important;
    letter-spacing: 3px;
    line-height: 1.8;
    font-size: var(--big-2-font);
}

.sample-text {
    opacity: 0;
    position: absolute;
    user-select: none;
    top: 0;
}
</style>