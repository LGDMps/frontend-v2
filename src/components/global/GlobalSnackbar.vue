<i18n>
{
	"en": {
		"clipboard": {
			"error": "Failed to copy to clipboard, please manually select text and copy it",
			"success": "Copied to clipboard"
		},
		"network": {
			"error": "Network error, please check your internet connection and try again."
		},
		"planner": {
			"calculationError": "Failed to calculate: {error}",
			"import": {
				"jsonError": "Failed to import: Data parsing error, please check your input ({error})",
				"success": "Successfully imported data for {amount} items"
			}
		},
		"pwaPopup": {
			"update": {
				"skipWaitingTimeout": "Failed to apply changes: ServiceWorker timed out. Please refresh page and try again"
			}
		}
	},
	"ja": {
		"clipboard": {
			"error": "",
			"success": ""
		},
		"network": {
			"error": ""
		},
		"planner": {
			"calculationError": "",
			"import": {
				"jsonError": "",
				"success": ""
			}
		},
		"pwaPopup": {
			"update": {
				"skipWaitingTimeout": ""
			}
		}
	},
	"ko": {
		"clipboard": {
			"error": "클립보드에 복사하지 못했습니다. 텍스트를 수동으로 선택하고 복사해주세요.",
			"success": "클립보드에 복사되었습니다."
		},
		"network": {
			"error": "네트워크 오류. 인터넷 연결을 확인한 후 다시 시도하세요."
		},
		"planner": {
			"calculationError": "계산오류: {error}",
			"import": {
				"jsonError": "가져오지 못했습니다. 데이터 구문 분석 오류입니다. 입력값을 확인해 주세요. ({error})",
				"success": "{amount}개 항목에 대한 데이터를 성공적으로 가져왔습니다."
			}
		},
		"pwaPopup": {
			"update": {
				"skipWaitingTimeout": "변경 내용을 적용하지 못했습니다. 서비스가 시간 초과되었습니다. 페이지를 새로 고친 후 다시 시도하세요."
			}
		}
	},
	"zh": {
		"clipboard": {
			"error": "复制到剪贴板失败，请手动复制",
			"success": "复制成功"
		},
		"network": {
			"error": "网络请求失败，请检查网络后重试"
		},
		"planner": {
			"calculationError": "计算失败：{error}",
			"import": {
				"jsonError": "导入失败：数据格式错误，请检查后重试（{error}）",
				"success": "导入成功：导入了 {amount} 个物品数据"
			}
		},
		"pwaPopup": {
			"update": {
				"skipWaitingTimeout": "更新失败：ServiceWorker 超时。请刷新页面重试"
			}
		}
	}
}
</i18n>

<template>
  <v-snackbar
    v-model="snackbar.enabled"
    bottom
    :timeout="snackbar.timeout"
    :color="snackbar.color"
  >
    <v-icon class="mr-4">
      {{ snackbar.icon }}
    </v-icon>
    {{ $t(snackbar.text, snackbar.extra) }}
    <v-spacer />
    <!--    <v-btn-->
    <!--      text-->
    <!--      @click="snackbar.enabled = false"-->
    <!--    >-->
    <!--      {{ $t('meta.dialog.close') }}-->
    <!--    </v-btn>-->
  </v-snackbar>
</template>

<script>
  import {mapState} from "vuex";

  export default {
    name: "GlobalSnackbar",
    computed: {
      ...mapState("ui", ["snackbar"])
    },
  }
</script>

<style scoped>

</style>