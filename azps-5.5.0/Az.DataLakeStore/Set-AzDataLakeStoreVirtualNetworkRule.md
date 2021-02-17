---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198122"
---
# <span data-ttu-id="2c21c-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2c21c-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="2c21c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c21c-102">SYNOPSIS</span></span>
<span data-ttu-id="2c21c-103">Modyfikuje określoną regułę sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c21c-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2c21c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c21c-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c21c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c21c-105">DESCRIPTION</span></span>
<span data-ttu-id="2c21c-106">Polecenie **cmdlet Set-AzDataLakeStoreVirtualNetworkRule** modyfikuje określoną regułę sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c21c-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="2c21c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c21c-107">EXAMPLES</span></span>

### <span data-ttu-id="2c21c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c21c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="2c21c-109">Aktualizacja identyfikatora podsieci wirtualnej reguły sieci wirtualnej "myVNET" w "dls" konta na "updatedId"</span><span class="sxs-lookup"><span data-stu-id="2c21c-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="2c21c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c21c-110">PARAMETERS</span></span>

### <span data-ttu-id="2c21c-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="2c21c-111">-Account</span></span>
<span data-ttu-id="2c21c-112">Konto usługi Data Lake Store w celu zaktualizowania reguły sieci wirtualnej w</span><span class="sxs-lookup"><span data-stu-id="2c21c-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="2c21c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c21c-113">-DefaultProfile</span></span>
<span data-ttu-id="2c21c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c21c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c21c-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2c21c-115">-Name</span></span>
<span data-ttu-id="2c21c-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2c21c-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="2c21c-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2c21c-117">-SubnetId</span></span>
<span data-ttu-id="2c21c-118">Początek prawidłowego zakresu adresów IP reguły sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2c21c-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="2c21c-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c21c-119">-Confirm</span></span>
<span data-ttu-id="2c21c-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c21c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c21c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c21c-121">-WhatIf</span></span>
<span data-ttu-id="2c21c-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c21c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c21c-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2c21c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c21c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c21c-124">CommonParameters</span></span>
<span data-ttu-id="2c21c-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c21c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c21c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c21c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c21c-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c21c-127">INPUTS</span></span>

### <span data-ttu-id="2c21c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2c21c-128">System.String</span></span>

## <span data-ttu-id="2c21c-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c21c-129">OUTPUTS</span></span>

### <span data-ttu-id="2c21c-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2c21c-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="2c21c-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c21c-131">NOTES</span></span>

## <span data-ttu-id="2c21c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c21c-132">RELATED LINKS</span></span>
