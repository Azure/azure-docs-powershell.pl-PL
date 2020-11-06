---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525097"
---
# <span data-ttu-id="fd04c-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="fd04c-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="fd04c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd04c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd04c-103">Pobiera zarejestrowane kategorie i ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="fd04c-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd04c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd04c-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd04c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fd04c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd04c-106">Polecenie cmdlet **Get-AzureRmDiagnosticSetting** pobiera kategorie i ziarno czasu rejestrowane dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd04c-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="fd04c-107">Ziarno czasu to interwał agregacji dla metryki.</span><span class="sxs-lookup"><span data-stu-id="fd04c-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="fd04c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd04c-108">EXAMPLES</span></span>

### <span data-ttu-id="fd04c-109">Przykład 1: uzyskiwanie statusu kategorii rejestrowania i ziaren czasowych</span><span class="sxs-lookup"><span data-stu-id="fd04c-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="fd04c-110">To polecenie pobiera kategorie i ziarno czasu rejestrowane w magazynie kluczy platformy Azure z identyfikatorem *zasobu* /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="fd04c-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="fd04c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd04c-111">PARAMETERS</span></span>

### <span data-ttu-id="fd04c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd04c-112">-DefaultProfile</span></span>
<span data-ttu-id="fd04c-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fd04c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd04c-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd04c-114">-ResourceId</span></span>
<span data-ttu-id="fd04c-115">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fd04c-115">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd04c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd04c-116">CommonParameters</span></span>
<span data-ttu-id="fd04c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd04c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd04c-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd04c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd04c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd04c-119">INPUTS</span></span>

### <span data-ttu-id="fd04c-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fd04c-120">None</span></span>
<span data-ttu-id="fd04c-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fd04c-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd04c-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd04c-122">OUTPUTS</span></span>

### <span data-ttu-id="fd04c-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="fd04c-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="fd04c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd04c-124">NOTES</span></span>

## <span data-ttu-id="fd04c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd04c-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd04c-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="fd04c-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


