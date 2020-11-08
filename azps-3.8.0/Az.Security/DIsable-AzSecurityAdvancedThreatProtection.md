---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 28e8521a283362989ff3ebace2f1e0a3e32c17a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052446"
---
# <span data-ttu-id="6c6a5-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6c6a5-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="6c6a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6a5-103">Wyłącza zasady zaawansowanej ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="6c6a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c6a5-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c6a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6c6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="6c6a5-106">`Disable-AzSecurityAdvancedThreatProtection`Polecenie cmdlet wyłącza zasady ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="6c6a5-107">Aby użyć tego polecenia cmdlet, określ parametr *ResourceID* .</span><span class="sxs-lookup"><span data-stu-id="6c6a5-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="6c6a5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c6a5-108">EXAMPLES</span></span>

### <span data-ttu-id="6c6a5-109">Przykład 1: konto magazynu</span><span class="sxs-lookup"><span data-stu-id="6c6a5-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="6c6a5-110">To polecenie wyłącza zaawansowane zasady ochrony przed zagrożeniami dla identyfikatora zasobu `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="6c6a5-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="6c6a5-111">Przykład 2: konto CosmosDB</span><span class="sxs-lookup"><span data-stu-id="6c6a5-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="6c6a5-112">To polecenie wyłącza zaawansowane zasady ochrony przed zagrożeniami dla identyfikatora zasobu ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="6c6a5-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="6c6a5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c6a5-113">PARAMETERS</span></span>

### <span data-ttu-id="6c6a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6a5-114">-DefaultProfile</span></span>
<span data-ttu-id="6c6a5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c6a5-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c6a5-116">-ResourceId</span></span>
<span data-ttu-id="6c6a5-117">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6c6a5-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c6a5-118">-Confirm</span></span>
<span data-ttu-id="6c6a5-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c6a5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c6a5-120">-WhatIf</span></span>
<span data-ttu-id="6c6a5-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c6a5-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c6a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6a5-123">CommonParameters</span></span>
<span data-ttu-id="6c6a5-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c6a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6a5-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c6a5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6a5-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c6a5-126">INPUTS</span></span>

### <span data-ttu-id="6c6a5-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6c6a5-127">None</span></span>

## <span data-ttu-id="6c6a5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c6a5-128">OUTPUTS</span></span>

### <span data-ttu-id="6c6a5-129">Microsoft. Azure. Commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="6c6a5-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="6c6a5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c6a5-130">NOTES</span></span>

## <span data-ttu-id="6c6a5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c6a5-131">RELATED LINKS</span></span>
