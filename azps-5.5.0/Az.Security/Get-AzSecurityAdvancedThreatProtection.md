---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242403"
---
# <span data-ttu-id="e7240-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e7240-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="e7240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7240-102">SYNOPSIS</span></span>
<span data-ttu-id="e7240-103">Pobiera zaawansowane zasady ochrony przed zagrożeniami dla konta magazynu/magazynu (db).</span><span class="sxs-lookup"><span data-stu-id="e7240-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="e7240-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7240-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7240-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7240-105">DESCRIPTION</span></span>
<span data-ttu-id="e7240-106">Polecenie `Get-AzSecurityAdvancedThreatProtection` cmdlet pobiera zasady ochrony przed zagrożeniami dla konta magazynu/magazynu (DB).</span><span class="sxs-lookup"><span data-stu-id="e7240-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="e7240-107">Aby użyć tego polecenia cmdlet, określ *parametr ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="e7240-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="e7240-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7240-108">EXAMPLES</span></span>

### <span data-ttu-id="e7240-109">Przykład 1. Konto magazynu</span><span class="sxs-lookup"><span data-stu-id="e7240-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="e7240-110">To polecenie pobiera zaawansowane zasady ochrony przed zagrożeniami dotyczące identyfikatora `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7240-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="e7240-111">Przykład 2. Konto Wschowa</span><span class="sxs-lookup"><span data-stu-id="e7240-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="e7240-112">To polecenie pobiera zaawansowane zasady ochrony przed zagrożeniami dotyczące identyfikatora ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7240-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="e7240-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7240-113">PARAMETERS</span></span>

### <span data-ttu-id="e7240-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7240-114">-DefaultProfile</span></span>
<span data-ttu-id="e7240-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7240-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7240-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7240-116">-ResourceId</span></span>
<span data-ttu-id="e7240-117">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="e7240-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e7240-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7240-118">CommonParameters</span></span>
<span data-ttu-id="e7240-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7240-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7240-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7240-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7240-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7240-121">INPUTS</span></span>

### <span data-ttu-id="e7240-122">System.String</span><span class="sxs-lookup"><span data-stu-id="e7240-122">System.String</span></span>

## <span data-ttu-id="e7240-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7240-123">OUTPUTS</span></span>

### <span data-ttu-id="e7240-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="e7240-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="e7240-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7240-125">NOTES</span></span>

## <span data-ttu-id="e7240-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7240-126">RELATED LINKS</span></span>
