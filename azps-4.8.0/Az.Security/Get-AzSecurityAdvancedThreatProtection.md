---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219262"
---
# <span data-ttu-id="f5362-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f5362-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f5362-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5362-102">SYNOPSIS</span></span>
<span data-ttu-id="f5362-103">Pobiera zaawansowaną zasadę ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f5362-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="f5362-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5362-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5362-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5362-105">DESCRIPTION</span></span>
<span data-ttu-id="f5362-106">`Get-AzSecurityAdvancedThreatProtection`Polecenie cmdlet pobiera zasady ochrony przed zagrożeniami dla konta magazynu/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f5362-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="f5362-107">Aby użyć tego polecenia cmdlet, określ parametr *ResourceID* .</span><span class="sxs-lookup"><span data-stu-id="f5362-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f5362-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5362-108">EXAMPLES</span></span>

### <span data-ttu-id="f5362-109">Przykład 1: konto magazynu</span><span class="sxs-lookup"><span data-stu-id="f5362-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f5362-110">To polecenie uzyskuje zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="f5362-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="f5362-111">Przykład 2: konto CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f5362-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="f5362-112">To polecenie uzyskuje zaawansowaną zasadę ochrony przed zagrożeniami dla identyfikatora zasobu ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="f5362-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="f5362-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5362-113">PARAMETERS</span></span>

### <span data-ttu-id="f5362-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5362-114">-DefaultProfile</span></span>
<span data-ttu-id="f5362-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5362-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5362-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5362-116">-ResourceId</span></span>
<span data-ttu-id="f5362-117">Identyfikator zasobu zabezpieczeń, dla którego ma zostać wywołane polecenie.</span><span class="sxs-lookup"><span data-stu-id="f5362-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f5362-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5362-118">CommonParameters</span></span>
<span data-ttu-id="f5362-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5362-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5362-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5362-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5362-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5362-121">INPUTS</span></span>

### <span data-ttu-id="f5362-122">System. String</span><span class="sxs-lookup"><span data-stu-id="f5362-122">System.String</span></span>

## <span data-ttu-id="f5362-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5362-123">OUTPUTS</span></span>

### <span data-ttu-id="f5362-124">Microsoft. Azure. Commands. Security. models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f5362-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f5362-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5362-125">NOTES</span></span>

## <span data-ttu-id="f5362-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5362-126">RELATED LINKS</span></span>
