---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376378"
---
# <span data-ttu-id="7c0ec-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c0ec-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="7c0ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0ec-103">Usuwa konto magazynu Edge dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="7c0ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c0ec-104">SYNTAX</span></span>

### <span data-ttu-id="7c0ec-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c0ec-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c0ec-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c0ec-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c0ec-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c0ec-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c0ec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7c0ec-108">DESCRIPTION</span></span>
<span data-ttu-id="7c0ec-109">Polecenie cmdlet **Remove-AzStackEdgeStorageAccount** usuwa powiązane konto magazynu z Edge na urządzeniu z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="7c0ec-110">Możesz określić nazwę konta magazynu granicznego, które ma zostać usunięte jako parametr w poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="7c0ec-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c0ec-111">EXAMPLES</span></span>

### <span data-ttu-id="7c0ec-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7c0ec-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="7c0ec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c0ec-113">PARAMETERS</span></span>

### <span data-ttu-id="7c0ec-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c0ec-114">-AsJob</span></span>
<span data-ttu-id="7c0ec-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7c0ec-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c0ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c0ec-116">-DefaultProfile</span></span>
<span data-ttu-id="7c0ec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c0ec-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7c0ec-118">-DeviceName</span></span>
<span data-ttu-id="7c0ec-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="7c0ec-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ec-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7c0ec-120">-InputObject</span></span>
<span data-ttu-id="7c0ec-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="7c0ec-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ec-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7c0ec-122">-Name</span></span>
<span data-ttu-id="7c0ec-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="7c0ec-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ec-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c0ec-124">-PassThru</span></span>
<span data-ttu-id="7c0ec-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="7c0ec-125">returns true if successful</span></span>

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

### <span data-ttu-id="7c0ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c0ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c0ec-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7c0ec-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ec-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c0ec-128">-ResourceId</span></span>
<span data-ttu-id="7c0ec-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="7c0ec-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c0ec-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7c0ec-130">-Confirm</span></span>
<span data-ttu-id="7c0ec-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c0ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c0ec-132">-WhatIf</span></span>
<span data-ttu-id="7c0ec-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c0ec-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c0ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0ec-135">CommonParameters</span></span>
<span data-ttu-id="7c0ec-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0ec-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c0ec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0ec-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c0ec-138">INPUTS</span></span>

### <span data-ttu-id="7c0ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7c0ec-139">System.String</span></span>

### <span data-ttu-id="7c0ec-140">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c0ec-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="7c0ec-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c0ec-141">OUTPUTS</span></span>

### <span data-ttu-id="7c0ec-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c0ec-142">System.Boolean</span></span>

## <span data-ttu-id="7c0ec-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c0ec-143">NOTES</span></span>

## <span data-ttu-id="7c0ec-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c0ec-144">RELATED LINKS</span></span>
