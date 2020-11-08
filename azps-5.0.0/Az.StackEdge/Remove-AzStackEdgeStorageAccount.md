---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234041"
---
# <span data-ttu-id="6c51d-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c51d-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6c51d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c51d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c51d-103">Usuwa konto magazynu Edge dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="6c51d-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="6c51d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c51d-104">SYNTAX</span></span>

### <span data-ttu-id="6c51d-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c51d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c51d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c51d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c51d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c51d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c51d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c51d-108">DESCRIPTION</span></span>
<span data-ttu-id="6c51d-109">Polecenie cmdlet **Remove-AzStackEdgeStorageAccount** usuwa powiązane konto magazynu z Edge na urządzeniu z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="6c51d-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="6c51d-110">Możesz określić nazwę konta magazynu granicznego, które ma zostać usunięte jako parametr w poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c51d-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="6c51d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c51d-111">EXAMPLES</span></span>

### <span data-ttu-id="6c51d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c51d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="6c51d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c51d-113">PARAMETERS</span></span>

### <span data-ttu-id="6c51d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c51d-114">-AsJob</span></span>
<span data-ttu-id="6c51d-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6c51d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c51d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c51d-116">-DefaultProfile</span></span>
<span data-ttu-id="6c51d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c51d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c51d-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6c51d-118">-DeviceName</span></span>
<span data-ttu-id="6c51d-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="6c51d-119">Device Name</span></span>

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

### <span data-ttu-id="6c51d-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6c51d-120">-InputObject</span></span>
<span data-ttu-id="6c51d-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="6c51d-121">Input Object</span></span>

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

### <span data-ttu-id="6c51d-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c51d-122">-Name</span></span>
<span data-ttu-id="6c51d-123">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="6c51d-123">Resource Name</span></span>

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

### <span data-ttu-id="6c51d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c51d-124">-PassThru</span></span>
<span data-ttu-id="6c51d-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="6c51d-125">returns true if successful</span></span>

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

### <span data-ttu-id="6c51d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c51d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6c51d-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6c51d-127">Resource Group Name</span></span>

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

### <span data-ttu-id="6c51d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c51d-128">-ResourceId</span></span>
<span data-ttu-id="6c51d-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6c51d-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="6c51d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c51d-130">-Confirm</span></span>
<span data-ttu-id="6c51d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c51d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c51d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c51d-132">-WhatIf</span></span>
<span data-ttu-id="6c51d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c51d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c51d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c51d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c51d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c51d-135">CommonParameters</span></span>
<span data-ttu-id="6c51d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c51d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c51d-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c51d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c51d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c51d-138">INPUTS</span></span>

### <span data-ttu-id="6c51d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c51d-139">System.String</span></span>

### <span data-ttu-id="6c51d-140">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c51d-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="6c51d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c51d-141">OUTPUTS</span></span>

### <span data-ttu-id="6c51d-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6c51d-142">System.Boolean</span></span>

## <span data-ttu-id="6c51d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c51d-143">NOTES</span></span>

## <span data-ttu-id="6c51d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c51d-144">RELATED LINKS</span></span>
