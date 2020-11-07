---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ad75f9ea973f80fb68955521a88a11b93fa61890
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710012"
---
# <span data-ttu-id="af23b-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af23b-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="af23b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af23b-102">SYNOPSIS</span></span>
<span data-ttu-id="af23b-103">Modyfikuje określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="af23b-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="af23b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af23b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af23b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af23b-105">DESCRIPTION</span></span>
<span data-ttu-id="af23b-106">Polecenie cmdlet **Set-AzDataLakeStoreVirtualNetworkRule** modyfikuje określoną regułę sieci wirtualnej w określonym sklepie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="af23b-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="af23b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af23b-107">EXAMPLES</span></span>

### <span data-ttu-id="af23b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af23b-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="af23b-109">Aktualizuje identyfikator podsieci reguły sieci wirtualnej "myVNET" na koncie "DLS" na "updatedId".</span><span class="sxs-lookup"><span data-stu-id="af23b-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="af23b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af23b-110">PARAMETERS</span></span>

### <span data-ttu-id="af23b-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="af23b-111">-Account</span></span>
<span data-ttu-id="af23b-112">Konto usługi Data Lake Store do aktualizowania reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="af23b-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="af23b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af23b-113">-DefaultProfile</span></span>
<span data-ttu-id="af23b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af23b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af23b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af23b-115">-Name</span></span>
<span data-ttu-id="af23b-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="af23b-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af23b-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="af23b-117">-SubnetId</span></span>
<span data-ttu-id="af23b-118">Początek prawidłowego zakresu adresów IP dla reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="af23b-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="af23b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af23b-119">-Confirm</span></span>
<span data-ttu-id="af23b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af23b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af23b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af23b-121">-WhatIf</span></span>
<span data-ttu-id="af23b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af23b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af23b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af23b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af23b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af23b-124">CommonParameters</span></span>
<span data-ttu-id="af23b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af23b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af23b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af23b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af23b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af23b-127">INPUTS</span></span>

### <span data-ttu-id="af23b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af23b-128">System.String</span></span>

## <span data-ttu-id="af23b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af23b-129">OUTPUTS</span></span>

### <span data-ttu-id="af23b-130">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="af23b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="af23b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af23b-131">NOTES</span></span>

## <span data-ttu-id="af23b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af23b-132">RELATED LINKS</span></span>
