---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e7195131830fd5b19a6d67b4fae5583374da7d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178651"
---
# <span data-ttu-id="77ffb-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="77ffb-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="77ffb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="77ffb-103">Wyłącza zaawansowane zasady ochrony przed zagrożeniami dla konta magazynu/dyskuDB.</span><span class="sxs-lookup"><span data-stu-id="77ffb-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="77ffb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77ffb-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ffb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="77ffb-105">DESCRIPTION</span></span>
<span data-ttu-id="77ffb-106">Polecenie `Disable-AzSecurityAdvancedThreatProtection` cmdlet wyłącza zasady ochrony przed zagrożeniami dla konta magazynu/magazynu (DB).</span><span class="sxs-lookup"><span data-stu-id="77ffb-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="77ffb-107">Aby użyć tego polecenia cmdlet, określ *parametr ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="77ffb-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="77ffb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77ffb-108">EXAMPLES</span></span>

### <span data-ttu-id="77ffb-109">Przykład 1. Konto magazynu</span><span class="sxs-lookup"><span data-stu-id="77ffb-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="77ffb-110">To polecenie wyłącza zaawansowane zasady ochrony przed zagrożeniami dotyczące identyfikatora `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="77ffb-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="77ffb-111">Przykład 2. Konto w Ułasdb</span><span class="sxs-lookup"><span data-stu-id="77ffb-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="77ffb-112">To polecenie wyłącza zaawansowane zasady ochrony przed zagrożeniami dotyczące identyfikatora ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` zasobu.</span><span class="sxs-lookup"><span data-stu-id="77ffb-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="77ffb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77ffb-113">PARAMETERS</span></span>

### <span data-ttu-id="77ffb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ffb-114">-DefaultProfile</span></span>
<span data-ttu-id="77ffb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77ffb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ffb-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77ffb-116">-ResourceId</span></span>
<span data-ttu-id="77ffb-117">Identyfikator zasobu zabezpieczeń, dla którego chcesz wywołać polecenie.</span><span class="sxs-lookup"><span data-stu-id="77ffb-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="77ffb-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77ffb-118">-Confirm</span></span>
<span data-ttu-id="77ffb-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77ffb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ffb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ffb-120">-WhatIf</span></span>
<span data-ttu-id="77ffb-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ffb-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77ffb-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="77ffb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ffb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ffb-123">CommonParameters</span></span>
<span data-ttu-id="77ffb-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ffb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ffb-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77ffb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ffb-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77ffb-126">INPUTS</span></span>

### <span data-ttu-id="77ffb-127">Brak</span><span class="sxs-lookup"><span data-stu-id="77ffb-127">None</span></span>

## <span data-ttu-id="77ffb-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77ffb-128">OUTPUTS</span></span>

### <span data-ttu-id="77ffb-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="77ffb-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="77ffb-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77ffb-130">NOTES</span></span>

## <span data-ttu-id="77ffb-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77ffb-131">RELATED LINKS</span></span>
