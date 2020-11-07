---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 4fccc705951ba944afdf13bf75d581e7c76d593f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705832"
---
# <span data-ttu-id="ce0f3-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce0f3-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ce0f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0f3-103">Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ce0f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce0f3-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce0f3-105">DESCRIPTION</span></span>
<span data-ttu-id="ce0f3-106">Polecenie cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** umożliwia dodanie reguły sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ce0f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce0f3-107">EXAMPLES</span></span>

### <span data-ttu-id="ce0f3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce0f3-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="ce0f3-109">Spowoduje to utworzenie nowej reguły sieci wirtualnej o nazwie "myVNET" w koncie "DLS" z identyfikatorem podsieci "testId".</span><span class="sxs-lookup"><span data-stu-id="ce0f3-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="ce0f3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce0f3-110">PARAMETERS</span></span>

### <span data-ttu-id="ce0f3-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ce0f3-111">-Account</span></span>
<span data-ttu-id="ce0f3-112">Konto usługi Data Lake Store umożliwiające dodanie reguły sieci wirtualnej do</span><span class="sxs-lookup"><span data-stu-id="ce0f3-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="ce0f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0f3-113">-DefaultProfile</span></span>
<span data-ttu-id="ce0f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce0f3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce0f3-115">-Name</span></span>
<span data-ttu-id="ce0f3-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ce0f3-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ce0f3-117">-SubnetId</span></span>
<span data-ttu-id="ce0f3-118">SubnetId reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ce0f3-118">The subnetId of the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0f3-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce0f3-119">-Confirm</span></span>
<span data-ttu-id="ce0f3-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0f3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0f3-121">-WhatIf</span></span>
<span data-ttu-id="ce0f3-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0f3-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0f3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0f3-124">CommonParameters</span></span>
<span data-ttu-id="ce0f3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0f3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0f3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0f3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0f3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce0f3-127">INPUTS</span></span>

### <span data-ttu-id="ce0f3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0f3-128">System.String</span></span>

## <span data-ttu-id="ce0f3-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce0f3-129">OUTPUTS</span></span>

### <span data-ttu-id="ce0f3-130">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce0f3-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ce0f3-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce0f3-131">NOTES</span></span>

## <span data-ttu-id="ce0f3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce0f3-132">RELATED LINKS</span></span>