---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977137"
---
# <span data-ttu-id="01ed0-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="01ed0-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="01ed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="01ed0-103">Pobiera określone reguły sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="01ed0-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="01ed0-104">Jeśli nie zostanie określona żadna reguła sieci wirtualnej, zostanie wymieniona lista wszystkich reguł sieci wirtualnej dla konta.</span><span class="sxs-lookup"><span data-stu-id="01ed0-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="01ed0-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="01ed0-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ed0-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="01ed0-106">DESCRIPTION</span></span>
<span data-ttu-id="01ed0-107">Polecenie Get-AzDataLakeStoreVirtualNetworkRule pobiera określone reguły sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="01ed0-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="01ed0-108">Jeśli nie zostanie określona żadna reguła sieci wirtualnej, zostanie wymieniona lista wszystkich reguł sieci wirtualnej dla konta.</span><span class="sxs-lookup"><span data-stu-id="01ed0-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="01ed0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="01ed0-109">EXAMPLES</span></span>

### <span data-ttu-id="01ed0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="01ed0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="01ed0-111">Zwraca regułę sieci wirtualnej o nazwie "myVNET" z konta "dls".</span><span class="sxs-lookup"><span data-stu-id="01ed0-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="01ed0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01ed0-112">PARAMETERS</span></span>

### <span data-ttu-id="01ed0-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="01ed0-113">-Account</span></span>
<span data-ttu-id="01ed0-114">Konto usługi Data Lake Store, z których można pobrać regułę sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="01ed0-114">The Data Lake Store account to get the virtual network rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ed0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ed0-115">-DefaultProfile</span></span>
<span data-ttu-id="01ed0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="01ed0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01ed0-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="01ed0-117">-Name</span></span>
<span data-ttu-id="01ed0-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="01ed0-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="01ed0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ed0-119">CommonParameters</span></span>
<span data-ttu-id="01ed0-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ed0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ed0-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ed0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ed0-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01ed0-122">INPUTS</span></span>

### <span data-ttu-id="01ed0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="01ed0-123">System.String</span></span>

## <span data-ttu-id="01ed0-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01ed0-124">OUTPUTS</span></span>

### <span data-ttu-id="01ed0-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="01ed0-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="01ed0-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="01ed0-126">NOTES</span></span>

## <span data-ttu-id="01ed0-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01ed0-127">RELATED LINKS</span></span>
