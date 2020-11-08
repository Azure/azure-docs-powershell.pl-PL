---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225063"
---
# <span data-ttu-id="a4380-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="a4380-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="a4380-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4380-102">SYNOPSIS</span></span>
<span data-ttu-id="a4380-103">Usuwanie zadania programu plan z subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="a4380-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="a4380-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4380-104">SYNTAX</span></span>

### <span data-ttu-id="a4380-105">BySubscriptionAndName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4380-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4380-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a4380-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4380-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="a4380-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4380-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4380-108">DESCRIPTION</span></span>
<span data-ttu-id="a4380-109">Usuwanie z listy planów przypisanych do abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a4380-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="a4380-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4380-110">EXAMPLES</span></span>

### <span data-ttu-id="a4380-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4380-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="a4380-112">Usuwanie zadania programu plan określonego na podstawie nazwy z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a4380-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="a4380-113">Przed wykonaniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4380-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="a4380-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4380-114">PARAMETERS</span></span>

### <span data-ttu-id="a4380-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4380-115">-DefaultProfile</span></span>
<span data-ttu-id="a4380-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4380-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4380-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4380-117">-InputObject</span></span>
<span data-ttu-id="a4380-118">Obiekt przydziału plany.</span><span class="sxs-lookup"><span data-stu-id="a4380-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4380-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a4380-119">-ManagementGroupId</span></span>
<span data-ttu-id="a4380-120">Identyfikator grupy zarządzania, w której jest zapisywane zadanie tworzenia pozycji plan.</span><span class="sxs-lookup"><span data-stu-id="a4380-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4380-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4380-121">-Name</span></span>
<span data-ttu-id="a4380-122">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="a4380-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4380-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4380-123">-PassThru</span></span>
<span data-ttu-id="a4380-124">Po ustawieniu polecenie cmdlet zwróci obiekt reprezentujący usunięte zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="a4380-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="a4380-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a4380-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4380-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a4380-126">-SubscriptionId</span></span>
<span data-ttu-id="a4380-127">Identyfikator subskrypcji, do której jest wdrażane zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="a4380-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4380-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4380-128">-Confirm</span></span>
<span data-ttu-id="a4380-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4380-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4380-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4380-130">-WhatIf</span></span>
<span data-ttu-id="a4380-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4380-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4380-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4380-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4380-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4380-133">CommonParameters</span></span>
<span data-ttu-id="a4380-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4380-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4380-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4380-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4380-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4380-136">INPUTS</span></span>

### <span data-ttu-id="a4380-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a4380-137">System.String</span></span>

### <span data-ttu-id="a4380-138">Microsoft. Azure. Commands. plan. modele. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="a4380-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="a4380-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4380-139">OUTPUTS</span></span>

### <span data-ttu-id="a4380-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="a4380-140">System.Object</span></span>
## <span data-ttu-id="a4380-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4380-141">NOTES</span></span>

## <span data-ttu-id="a4380-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4380-142">RELATED LINKS</span></span>
