---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541723"
---
# <span data-ttu-id="f7157-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7157-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="f7157-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7157-102">SYNOPSIS</span></span>
<span data-ttu-id="f7157-103">Pobiera określone reguły sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7157-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f7157-104">Jeśli nie określono żadnej reguły sieci wirtualnej, wyświetlane są wszystkie reguły sieci wirtualnej dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f7157-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7157-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7157-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7157-106">Opis</span><span class="sxs-lookup"><span data-stu-id="f7157-106">DESCRIPTION</span></span>
<span data-ttu-id="f7157-107">Polecenie cmdlet Get-AzureRmDataLakeStoreVirtualNetworkRule pobiera określone reguły sieci wirtualnej w określonej usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f7157-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="f7157-108">Jeśli nie określono żadnej reguły sieci wirtualnej, wyświetlane są wszystkie reguły sieci wirtualnej dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="f7157-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="f7157-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7157-109">EXAMPLES</span></span>

### <span data-ttu-id="f7157-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7157-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="f7157-111">Zwraca regułę sieci wirtualnej o nazwie "myVNET" z konta "DLS".</span><span class="sxs-lookup"><span data-stu-id="f7157-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="f7157-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7157-112">PARAMETERS</span></span>

### <span data-ttu-id="f7157-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="f7157-113">-Account</span></span>
<span data-ttu-id="f7157-114">Konto usługi Data Lake Store do pobierania reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f7157-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="f7157-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7157-115">-DefaultProfile</span></span>
<span data-ttu-id="f7157-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7157-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7157-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7157-117">-Name</span></span>
<span data-ttu-id="f7157-118">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7157-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="f7157-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7157-119">CommonParameters</span></span>
<span data-ttu-id="f7157-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7157-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7157-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7157-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7157-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7157-122">INPUTS</span></span>

### <span data-ttu-id="f7157-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f7157-123">System.String</span></span>

## <span data-ttu-id="f7157-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7157-124">OUTPUTS</span></span>

### <span data-ttu-id="f7157-125">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f7157-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="f7157-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7157-126">NOTES</span></span>

## <span data-ttu-id="f7157-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7157-127">RELATED LINKS</span></span>
