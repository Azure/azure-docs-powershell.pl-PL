---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 41923067729b50a77f8660a7f626ac464619aa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867320"
---
# <span data-ttu-id="01951-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="01951-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="01951-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01951-102">SYNOPSIS</span></span>
<span data-ttu-id="01951-103">Pobiera zarejestrowane kategorie i ziarno czasu.</span><span class="sxs-lookup"><span data-stu-id="01951-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="01951-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01951-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01951-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01951-105">DESCRIPTION</span></span>
<span data-ttu-id="01951-106">Polecenie cmdlet **Get-AzDiagnosticSetting** pobiera kategorie i ziarno czasu rejestrowane dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="01951-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="01951-107">Ziarno czasu to interwał agregacji dla metryki.</span><span class="sxs-lookup"><span data-stu-id="01951-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="01951-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01951-108">EXAMPLES</span></span>

### <span data-ttu-id="01951-109">Przykład 1: uzyskiwanie statusu kategorii rejestrowania i ziaren czasowych</span><span class="sxs-lookup"><span data-stu-id="01951-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="01951-110">To polecenie pobiera kategorie i ziarno czasu rejestrowane w magazynie kluczy platformy Azure z identyfikatorem *zasobu* /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="01951-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="01951-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01951-111">PARAMETERS</span></span>

### <span data-ttu-id="01951-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01951-112">-DefaultProfile</span></span>
<span data-ttu-id="01951-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="01951-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01951-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01951-114">-Name</span></span>
<span data-ttu-id="01951-115">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="01951-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="01951-116">Jeśli na liście nie ma domyślnie "usługa", jak w poprzednim interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="01951-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="01951-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01951-117">-ResourceId</span></span>
<span data-ttu-id="01951-118">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="01951-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="01951-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01951-119">CommonParameters</span></span>
<span data-ttu-id="01951-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01951-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01951-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01951-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01951-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01951-122">INPUTS</span></span>

### <span data-ttu-id="01951-123">System. String</span><span class="sxs-lookup"><span data-stu-id="01951-123">System.String</span></span>

## <span data-ttu-id="01951-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01951-124">OUTPUTS</span></span>

### <span data-ttu-id="01951-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="01951-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="01951-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01951-126">NOTES</span></span>

## <span data-ttu-id="01951-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01951-127">RELATED LINKS</span></span>

<span data-ttu-id="01951-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="01951-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
