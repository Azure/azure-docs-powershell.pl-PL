---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
ms.openlocfilehash: eb7dbdee5d1d3d1574be30c5168d97dfcee6ab27
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897458"
---
# <span data-ttu-id="977c6-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="977c6-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="977c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="977c6-102">SYNOPSIS</span></span>
<span data-ttu-id="977c6-103">Pobiera zarejestrowane kategorie i ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="977c6-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="977c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="977c6-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="977c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="977c6-105">DESCRIPTION</span></span>
<span data-ttu-id="977c6-106">Polecenie cmdlet **Get-AzureRmDiagnosticSetting** pobiera kategorie i ziarno czasu rejestrowane dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="977c6-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="977c6-107">Ziarno czasu to interwał agregacji dla metryki.</span><span class="sxs-lookup"><span data-stu-id="977c6-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="977c6-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="977c6-108">EXAMPLES</span></span>

### <span data-ttu-id="977c6-109">Przykład 1: uzyskiwanie statusu kategorii rejestrowania i ziaren czasowych</span><span class="sxs-lookup"><span data-stu-id="977c6-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="977c6-110">To polecenie pobiera kategorie i ziarno czasu rejestrowane w magazynie kluczy platformy Azure z identyfikatorem *zasobu* /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="977c6-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="977c6-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="977c6-111">PARAMETERS</span></span>

### <span data-ttu-id="977c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977c6-112">-DefaultProfile</span></span>
<span data-ttu-id="977c6-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="977c6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977c6-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="977c6-114">-Name</span></span>
<span data-ttu-id="977c6-115">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="977c6-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="977c6-116">Jeśli na liście nie ma domyślnie "usługa", jak w poprzednim interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="977c6-116">If not given the call default to "service" as it was in the previous API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="977c6-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="977c6-117">-ResourceId</span></span>
<span data-ttu-id="977c6-118">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="977c6-118">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="977c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977c6-119">CommonParameters</span></span>
<span data-ttu-id="977c6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977c6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977c6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977c6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="977c6-122">INPUTS</span></span>

### <span data-ttu-id="977c6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="977c6-123">System.String</span></span>

## <span data-ttu-id="977c6-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="977c6-124">OUTPUTS</span></span>

### <span data-ttu-id="977c6-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="977c6-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="977c6-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="977c6-126">NOTES</span></span>

## <span data-ttu-id="977c6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="977c6-127">RELATED LINKS</span></span>

<span data-ttu-id="977c6-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="977c6-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
