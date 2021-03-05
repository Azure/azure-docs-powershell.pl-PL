---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980065"
---
# <span data-ttu-id="e9615-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e9615-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="e9615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9615-102">SYNOPSIS</span></span>
<span data-ttu-id="e9615-103">Pobiera zarejestrowane kategorie i czas.</span><span class="sxs-lookup"><span data-stu-id="e9615-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="e9615-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9615-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9615-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9615-105">DESCRIPTION</span></span>
<span data-ttu-id="e9615-106">Polecenie **cmdlet Get-AzDiagnosticSetting** pobiera kategorie i czasowe, które są rejestrowane dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="e9615-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="e9615-107">Przedział czasu to interwał agregacji metryki.</span><span class="sxs-lookup"><span data-stu-id="e9615-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="e9615-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9615-108">EXAMPLES</span></span>

### <span data-ttu-id="e9615-109">Przykład 1. Uzyskiwanie stanu kategorii rejestrowania i okresów</span><span class="sxs-lookup"><span data-stu-id="e9615-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="e9615-110">To polecenie pobiera kategorie i stopnie czasu rejestrowane dla magazynu kluczy platformy Azure z polem *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="e9615-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="e9615-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9615-111">PARAMETERS</span></span>

### <span data-ttu-id="e9615-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9615-112">-DefaultProfile</span></span>
<span data-ttu-id="e9615-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e9615-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9615-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e9615-114">-Name</span></span>
<span data-ttu-id="e9615-115">Nazwa ustawienia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="e9615-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="e9615-116">Jeśli nie nadano domyślnego ustawienia "service" (usługa), jak w poprzednim interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="e9615-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="e9615-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9615-117">-ResourceId</span></span>
<span data-ttu-id="e9615-118">Określa identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e9615-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="e9615-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9615-119">CommonParameters</span></span>
<span data-ttu-id="e9615-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9615-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9615-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9615-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9615-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9615-122">INPUTS</span></span>

### <span data-ttu-id="e9615-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e9615-123">System.String</span></span>

## <span data-ttu-id="e9615-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9615-124">OUTPUTS</span></span>

### <span data-ttu-id="e9615-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="e9615-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="e9615-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9615-126">NOTES</span></span>

## <span data-ttu-id="e9615-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9615-127">RELATED LINKS</span></span>

<span data-ttu-id="e9615-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="e9615-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
