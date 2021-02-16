---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194682"
---
# <span data-ttu-id="5bd1f-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bd1f-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="5bd1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd1f-103">Dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5bd1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5bd1f-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bd1f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd1f-106">Polecenie **cmdlet Add-AzDataLakeStoreVirtualNetworkRule** dodaje regułę sieci wirtualnej do określonego konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="5bd1f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5bd1f-107">EXAMPLES</span></span>

### <span data-ttu-id="5bd1f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5bd1f-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="5bd1f-109">Powoduje to utworzenie nowej reguły sieci wirtualnej o nazwie "myVNET" w "dls" konta z identyfikatorem podsieci "testId"</span><span class="sxs-lookup"><span data-stu-id="5bd1f-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="5bd1f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bd1f-110">PARAMETERS</span></span>

### <span data-ttu-id="5bd1f-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="5bd1f-111">-Account</span></span>
<span data-ttu-id="5bd1f-112">Konto usługi Data Lake Store w celu dodania reguły sieci wirtualnej do</span><span class="sxs-lookup"><span data-stu-id="5bd1f-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="5bd1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd1f-113">-DefaultProfile</span></span>
<span data-ttu-id="5bd1f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bd1f-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5bd1f-115">-Name</span></span>
<span data-ttu-id="5bd1f-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="5bd1f-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5bd1f-117">-SubnetId</span></span>
<span data-ttu-id="5bd1f-118">The subnetId of the virtual network rule</span><span class="sxs-lookup"><span data-stu-id="5bd1f-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="5bd1f-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bd1f-119">-Confirm</span></span>
<span data-ttu-id="5bd1f-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bd1f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bd1f-121">-WhatIf</span></span>
<span data-ttu-id="5bd1f-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bd1f-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bd1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd1f-124">CommonParameters</span></span>
<span data-ttu-id="5bd1f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bd1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd1f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd1f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd1f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bd1f-127">INPUTS</span></span>

### <span data-ttu-id="5bd1f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5bd1f-128">System.String</span></span>

## <span data-ttu-id="5bd1f-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bd1f-129">OUTPUTS</span></span>

### <span data-ttu-id="5bd1f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5bd1f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="5bd1f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5bd1f-131">NOTES</span></span>

## <span data-ttu-id="5bd1f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bd1f-132">RELATED LINKS</span></span>
