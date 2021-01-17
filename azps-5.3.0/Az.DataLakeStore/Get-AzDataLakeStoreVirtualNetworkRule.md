---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489134"
---
# <span data-ttu-id="1e69c-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e69c-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1e69c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e69c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e69c-103">Pobiera określone reguły sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e69c-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1e69c-104">Jeśli nie określono żadnej reguły sieci wirtualnej, wyświetlane są wszystkie reguły sieci wirtualnej dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="1e69c-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="1e69c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e69c-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e69c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="1e69c-106">DESCRIPTION</span></span>
<span data-ttu-id="1e69c-107">Polecenie cmdlet Get-AzDataLakeStoreVirtualNetworkRule pobiera określone reguły sieci wirtualnej w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e69c-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1e69c-108">Jeśli nie określono żadnej reguły sieci wirtualnej, wyświetlane są wszystkie reguły sieci wirtualnej dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="1e69c-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="1e69c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e69c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e69c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e69c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="1e69c-111">Zwraca regułę sieci wirtualnej o nazwie "myVNET" z konta "DLS".</span><span class="sxs-lookup"><span data-stu-id="1e69c-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="1e69c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e69c-112">PARAMETERS</span></span>

### <span data-ttu-id="1e69c-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="1e69c-113">-Account</span></span>
<span data-ttu-id="1e69c-114">Konto usługi Data Lake Store do pobierania reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="1e69c-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="1e69c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e69c-115">-DefaultProfile</span></span>
<span data-ttu-id="1e69c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e69c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e69c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e69c-117">-Name</span></span>
<span data-ttu-id="1e69c-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1e69c-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1e69c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e69c-119">CommonParameters</span></span>
<span data-ttu-id="1e69c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e69c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e69c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e69c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e69c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e69c-122">INPUTS</span></span>

### <span data-ttu-id="1e69c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1e69c-123">System.String</span></span>

## <span data-ttu-id="1e69c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e69c-124">OUTPUTS</span></span>

### <span data-ttu-id="1e69c-125">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e69c-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1e69c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e69c-126">NOTES</span></span>

## <span data-ttu-id="1e69c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e69c-127">RELATED LINKS</span></span>
