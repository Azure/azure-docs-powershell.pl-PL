---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180907"
---
# <span data-ttu-id="de4d9-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="de4d9-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="de4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="de4d9-103">Usuwa określoną regułę sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de4d9-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="de4d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de4d9-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de4d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="de4d9-106">Polecenie **cmdlet Remove-AzDataLakeStoreVirtualNetworkRule** usuwa określoną regułę sieci wirtualnej w określonym magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="de4d9-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="de4d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="de4d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de4d9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="de4d9-109">Usuwa regułę sieci wirtualnej "myVNET" z konta "dls"</span><span class="sxs-lookup"><span data-stu-id="de4d9-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="de4d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de4d9-110">PARAMETERS</span></span>

### <span data-ttu-id="de4d9-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="de4d9-111">-Account</span></span>
<span data-ttu-id="de4d9-112">Konto usługi Data Lake Store w celu zaktualizowania reguły sieci wirtualnej w</span><span class="sxs-lookup"><span data-stu-id="de4d9-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="de4d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4d9-113">-DefaultProfile</span></span>
<span data-ttu-id="de4d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de4d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de4d9-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="de4d9-115">-Name</span></span>
<span data-ttu-id="de4d9-116">Nazwa reguły sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="de4d9-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="de4d9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de4d9-117">-PassThru</span></span>
<span data-ttu-id="de4d9-118">Wskazuje, że powinna zostać zwrócona odpowiedź logiczna wskazująca wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="de4d9-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4d9-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de4d9-119">-Confirm</span></span>
<span data-ttu-id="de4d9-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="de4d9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4d9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4d9-121">-WhatIf</span></span>
<span data-ttu-id="de4d9-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de4d9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4d9-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="de4d9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4d9-124">CommonParameters</span></span>
<span data-ttu-id="de4d9-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de4d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4d9-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4d9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4d9-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de4d9-127">INPUTS</span></span>

### <span data-ttu-id="de4d9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="de4d9-128">System.String</span></span>

## <span data-ttu-id="de4d9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de4d9-129">OUTPUTS</span></span>

### <span data-ttu-id="de4d9-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de4d9-130">System.Boolean</span></span>

## <span data-ttu-id="de4d9-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de4d9-131">NOTES</span></span>

## <span data-ttu-id="de4d9-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de4d9-132">RELATED LINKS</span></span>
