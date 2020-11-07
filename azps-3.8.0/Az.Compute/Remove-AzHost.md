---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896798"
---
# <span data-ttu-id="13145-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="13145-101">Remove-AzHost</span></span>

## <span data-ttu-id="13145-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13145-102">SYNOPSIS</span></span>
<span data-ttu-id="13145-103">Usuwa hosta.</span><span class="sxs-lookup"><span data-stu-id="13145-103">Removes a host.</span></span>

## <span data-ttu-id="13145-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13145-104">SYNTAX</span></span>

### <span data-ttu-id="13145-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="13145-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13145-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="13145-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13145-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="13145-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13145-108">Opis</span><span class="sxs-lookup"><span data-stu-id="13145-108">DESCRIPTION</span></span>
<span data-ttu-id="13145-109">To polecenie cmdlet spowoduje usunięcie hosta</span><span class="sxs-lookup"><span data-stu-id="13145-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="13145-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13145-110">EXAMPLES</span></span>

### <span data-ttu-id="13145-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13145-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="13145-112">To polecenie pobiera i usuwa danego hosta.</span><span class="sxs-lookup"><span data-stu-id="13145-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="13145-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="13145-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="13145-114">To polecenie umożliwia usunięcie danego hosta.</span><span class="sxs-lookup"><span data-stu-id="13145-114">This command removes the given host.</span></span>

## <span data-ttu-id="13145-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13145-115">PARAMETERS</span></span>

### <span data-ttu-id="13145-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13145-116">-AsJob</span></span>
<span data-ttu-id="13145-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="13145-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13145-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13145-118">-DefaultProfile</span></span>
<span data-ttu-id="13145-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13145-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13145-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="13145-120">-HostGroupName</span></span>
<span data-ttu-id="13145-121">Nazwa grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="13145-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13145-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="13145-122">-InputObject</span></span>
<span data-ttu-id="13145-123">Lokalny obiekt hosta.</span><span class="sxs-lookup"><span data-stu-id="13145-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13145-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13145-124">-Name</span></span>
<span data-ttu-id="13145-125">Nazwa hosta.</span><span class="sxs-lookup"><span data-stu-id="13145-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13145-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13145-126">-ResourceGroupName</span></span>
<span data-ttu-id="13145-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13145-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13145-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13145-128">-ResourceId</span></span>
<span data-ttu-id="13145-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="13145-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13145-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13145-130">-Confirm</span></span>
<span data-ttu-id="13145-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13145-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13145-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13145-132">-WhatIf</span></span>
<span data-ttu-id="13145-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13145-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13145-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13145-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13145-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13145-135">CommonParameters</span></span>
<span data-ttu-id="13145-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13145-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13145-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13145-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13145-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13145-138">INPUTS</span></span>

### <span data-ttu-id="13145-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13145-139">System.String</span></span>

### <span data-ttu-id="13145-140">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHost</span><span class="sxs-lookup"><span data-stu-id="13145-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="13145-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13145-141">OUTPUTS</span></span>

### <span data-ttu-id="13145-142">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="13145-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="13145-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13145-143">NOTES</span></span>

## <span data-ttu-id="13145-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13145-144">RELATED LINKS</span></span>
