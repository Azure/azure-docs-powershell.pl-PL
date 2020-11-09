---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/stop-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Stop-AzDataBoxJob.md
ms.openlocfilehash: 8e069dfe13ed060c80f884b93317148e7e6ec646
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94306636"
---
# <span data-ttu-id="9ad04-101">Stop-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9ad04-101">Stop-AzDataBoxJob</span></span>

## <span data-ttu-id="9ad04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ad04-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad04-103">Anuluje bieżące zadanie DATAbox, jeśli zadanie jest w stanie anulowanie.</span><span class="sxs-lookup"><span data-stu-id="9ad04-103">Cancels an ongoing databox job if the job is in cancellable state.</span></span>

## <span data-ttu-id="9ad04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ad04-104">SYNTAX</span></span>

### <span data-ttu-id="9ad04-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ad04-105">GetByNameParameterSet (Default)</span></span>
```
Stop-AzDataBoxJob -ResourceGroupName <String> -Name <String> -Reason <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad04-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad04-106">GetByResourceIdParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad04-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad04-107">GetByInputObjectParameterSet</span></span>
```
Stop-AzDataBoxJob -Reason <String> -InputObject <PSDataBoxJob> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad04-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9ad04-108">DESCRIPTION</span></span>
<span data-ttu-id="9ad04-109">Polecenie cmdlet **stop-AzDataBoxJob** służy do anulowania zadania DATAbox.</span><span class="sxs-lookup"><span data-stu-id="9ad04-109">The **Stop-AzDataBoxJob** cmdlet is used to cancel a databox job.</span></span>

## <span data-ttu-id="9ad04-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ad04-110">EXAMPLES</span></span>

### <span data-ttu-id="9ad04-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ad04-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random"
Confirm
"Removing Databox Job "test
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

```

<span data-ttu-id="9ad04-112">Anuluje określone zadanie DATAbox.</span><span class="sxs-lookup"><span data-stu-id="9ad04-112">Cancels the specified databox job</span></span>

### <span data-ttu-id="9ad04-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9ad04-113">Example 2</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceGroupName "TestRg" -name "test" -Reason "Random" -Force

```

<span data-ttu-id="9ad04-114">Anuluje określone zadanie DATAbox bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="9ad04-114">Cancels the specified databox job forcefully without confirmation</span></span>

### <span data-ttu-id="9ad04-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9ad04-115">Example 3</span></span>
```powershell
PS C:\> Stop-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg/providers/Microsoft.DataBox/jobs/test"

```

<span data-ttu-id="9ad04-116">Anuluje określone zadanie DATAbox.</span><span class="sxs-lookup"><span data-stu-id="9ad04-116">Cancels the specified databox job</span></span>

## <span data-ttu-id="9ad04-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ad04-117">PARAMETERS</span></span>

### <span data-ttu-id="9ad04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad04-118">-DefaultProfile</span></span>
<span data-ttu-id="9ad04-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ad04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad04-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ad04-120">-Force</span></span>
<span data-ttu-id="9ad04-121">Wymuszaj zatrzymanie bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="9ad04-121">Force stop without confirmation</span></span>

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

### <span data-ttu-id="9ad04-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ad04-122">-InputObject</span></span>
<span data-ttu-id="9ad04-123">Inputobject typu PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9ad04-123">InputObject of type PSDataBoxJob</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad04-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ad04-124">-Name</span></span>
<span data-ttu-id="9ad04-125">Nazwa zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="9ad04-125">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad04-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ad04-126">-PassThru</span></span>
<span data-ttu-id="9ad04-127">PassThru</span><span class="sxs-lookup"><span data-stu-id="9ad04-127">PassThru</span></span>

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

### <span data-ttu-id="9ad04-128">-Przyczyna</span><span class="sxs-lookup"><span data-stu-id="9ad04-128">-Reason</span></span>
<span data-ttu-id="9ad04-129">Przyczyna anulowania</span><span class="sxs-lookup"><span data-stu-id="9ad04-129">Reason For Cancellation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad04-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad04-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ad04-131">Nazwa grupy zasobów zadania DATAbox</span><span class="sxs-lookup"><span data-stu-id="9ad04-131">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ad04-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ad04-132">-ResourceId</span></span>
<span data-ttu-id="9ad04-133">Identyfikator zasobu DATAbox</span><span class="sxs-lookup"><span data-stu-id="9ad04-133">Databox Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad04-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ad04-134">-Confirm</span></span>
<span data-ttu-id="9ad04-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ad04-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad04-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad04-136">-WhatIf</span></span>
<span data-ttu-id="9ad04-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ad04-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ad04-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ad04-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad04-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad04-139">CommonParameters</span></span>
<span data-ttu-id="9ad04-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad04-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad04-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ad04-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad04-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ad04-142">INPUTS</span></span>

### <span data-ttu-id="9ad04-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad04-143">System.String</span></span>

## <span data-ttu-id="9ad04-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ad04-144">OUTPUTS</span></span>

### <span data-ttu-id="9ad04-145">System. void</span><span class="sxs-lookup"><span data-stu-id="9ad04-145">System.Void</span></span>

## <span data-ttu-id="9ad04-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ad04-146">NOTES</span></span>

## <span data-ttu-id="9ad04-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ad04-147">RELATED LINKS</span></span>
