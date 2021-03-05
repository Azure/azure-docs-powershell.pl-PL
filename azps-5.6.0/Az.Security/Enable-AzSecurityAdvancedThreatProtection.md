---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986595"
---
# <span data-ttu-id="4bdee-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4bdee-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="4bdee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdee-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdee-103">Umożliwia korzystanie z zaawansowanych zasad ochrony przed zagrożeniami dla konta magazynu/magazynu (DB).</span><span class="sxs-lookup"><span data-stu-id="4bdee-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="4bdee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4bdee-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdee-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4bdee-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdee-106">Polecenie cmdlet umożliwia korzystanie z zasad ochrony przed zagrożeniami `Enable-AzSecurityAdvancedThreatProtection` dla konta magazynu/magazynu (DB).</span><span class="sxs-lookup"><span data-stu-id="4bdee-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="4bdee-107">Aby użyć tego polecenia cmdlet, określ *parametr ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="4bdee-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="4bdee-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4bdee-108">EXAMPLES</span></span>

### <span data-ttu-id="4bdee-109">Przykład 1. Konto magazynu</span><span class="sxs-lookup"><span data-stu-id="4bdee-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="4bdee-110">To polecenie umożliwia korzystanie z zaawansowanych zasad ochrony przed zagrożeniami dla identyfikatora `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="4bdee-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="4bdee-111">Przykład 2. Konto Wsad.</span><span class="sxs-lookup"><span data-stu-id="4bdee-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="4bdee-112">To polecenie umożliwia korzystanie z zaawansowanych zasad ochrony przed zagrożeniami dla identyfikatora ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="4bdee-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="4bdee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bdee-113">PARAMETERS</span></span>

### <span data-ttu-id="4bdee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdee-114">-DefaultProfile</span></span>
<span data-ttu-id="4bdee-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bdee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdee-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bdee-116">-ResourceId</span></span>
<span data-ttu-id="4bdee-117">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="4bdee-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bdee-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bdee-118">-Confirm</span></span>
<span data-ttu-id="4bdee-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4bdee-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdee-120">-WhatIf</span></span>
<span data-ttu-id="4bdee-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bdee-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bdee-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4bdee-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bdee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdee-123">CommonParameters</span></span>
<span data-ttu-id="4bdee-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdee-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bdee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdee-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bdee-126">INPUTS</span></span>

### <span data-ttu-id="4bdee-127">Brak</span><span class="sxs-lookup"><span data-stu-id="4bdee-127">None</span></span>

## <span data-ttu-id="4bdee-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bdee-128">OUTPUTS</span></span>

### <span data-ttu-id="4bdee-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4bdee-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="4bdee-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4bdee-130">NOTES</span></span>

## <span data-ttu-id="4bdee-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bdee-131">RELATED LINKS</span></span>
