---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503086"
---
# <span data-ttu-id="4c490-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4c490-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="4c490-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c490-102">SYNOPSIS</span></span>
<span data-ttu-id="4c490-103">Włącza zaawansowane zasady ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4c490-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="4c490-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c490-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c490-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c490-105">DESCRIPTION</span></span>
<span data-ttu-id="4c490-106">`Enable-AzSecurityAdvancedThreatProtection`Polecenie cmdlet włącza zasady ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="4c490-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="4c490-107">Aby użyć tego polecenia cmdlet, określ parametr *ResourceID* .</span><span class="sxs-lookup"><span data-stu-id="4c490-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="4c490-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c490-108">EXAMPLES</span></span>

### <span data-ttu-id="4c490-109">Przykład 1: konto magazynu</span><span class="sxs-lookup"><span data-stu-id="4c490-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="4c490-110">To polecenie włącza zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="4c490-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="4c490-111">Przykład 2: konto CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4c490-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="4c490-112">To polecenie włącza zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="4c490-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="4c490-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c490-113">PARAMETERS</span></span>

### <span data-ttu-id="4c490-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c490-114">-DefaultProfile</span></span>
<span data-ttu-id="4c490-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c490-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c490-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c490-116">-ResourceId</span></span>
<span data-ttu-id="4c490-117">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="4c490-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4c490-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c490-118">-Confirm</span></span>
<span data-ttu-id="4c490-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c490-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c490-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c490-120">-WhatIf</span></span>
<span data-ttu-id="4c490-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c490-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c490-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c490-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c490-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c490-123">CommonParameters</span></span>
<span data-ttu-id="4c490-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c490-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c490-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c490-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c490-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c490-126">INPUTS</span></span>

### <span data-ttu-id="4c490-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4c490-127">None</span></span>

## <span data-ttu-id="4c490-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c490-128">OUTPUTS</span></span>

### <span data-ttu-id="4c490-129">Microsoft. Azure. Commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4c490-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="4c490-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c490-130">NOTES</span></span>

## <span data-ttu-id="4c490-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c490-131">RELATED LINKS</span></span>
