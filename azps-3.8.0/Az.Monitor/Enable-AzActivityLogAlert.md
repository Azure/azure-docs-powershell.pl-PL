---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: f1af25ca59b6af6a9712019d541e68c269609242
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409192"
---
# <span data-ttu-id="a529f-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a529f-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="a529f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a529f-102">SYNOPSIS</span></span>
<span data-ttu-id="a529f-103">Włącza alert dziennika aktywności i ustawia jego tagi.</span><span class="sxs-lookup"><span data-stu-id="a529f-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="a529f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a529f-104">SYNTAX</span></span>

### <span data-ttu-id="a529f-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a529f-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a529f-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="a529f-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a529f-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="a529f-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a529f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a529f-108">DESCRIPTION</span></span>
<span data-ttu-id="a529f-109">Polecenie **cmdlet Enable-AzActivityLogAlert** umożliwia włączenie alertu dziennika aktywności i ustawienie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="a529f-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="a529f-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed wykonaniem poprawek dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="a529f-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a529f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a529f-111">EXAMPLES</span></span>

### <span data-ttu-id="a529f-112">Przykład 1. Włączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="a529f-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a529f-113">To polecenie włącza alert dziennika działań o nazwie alert1 w grupie zasobów Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="a529f-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="a529f-114">Przykład 2. Włączanie alertu dziennika aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="a529f-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a529f-115">To polecenie włącza alert dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="a529f-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="a529f-116">W tym celu jako argument wejściowy jest używany obiekt PSActivityLogAlertResource.</span><span class="sxs-lookup"><span data-stu-id="a529f-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a529f-117">Przykład 3. Włączanie parametru ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="a529f-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="a529f-118">To polecenie włącza parametr ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="a529f-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a529f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a529f-119">PARAMETERS</span></span>

### <span data-ttu-id="a529f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a529f-120">-DefaultProfile</span></span>
<span data-ttu-id="a529f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a529f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a529f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a529f-122">-InputObject</span></span>
<span data-ttu-id="a529f-123">Ustawia właściwość tagów InputObject połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i opcjonalnych właściwości tagów.</span><span class="sxs-lookup"><span data-stu-id="a529f-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a529f-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a529f-124">-Name</span></span>
<span data-ttu-id="a529f-125">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a529f-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a529f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a529f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a529f-127">Nazwa grupy zasobów, w której ma istnieć zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="a529f-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a529f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a529f-128">-ResourceId</span></span>
<span data-ttu-id="a529f-129">Ustawia właściwość tagów ResourceId połączenia w celu wyodrębnienia wymaganej nazwy, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a529f-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a529f-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a529f-130">-Confirm</span></span>
<span data-ttu-id="a529f-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a529f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a529f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a529f-132">-WhatIf</span></span>
<span data-ttu-id="a529f-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a529f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a529f-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a529f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a529f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a529f-135">CommonParameters</span></span>
<span data-ttu-id="a529f-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a529f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a529f-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a529f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a529f-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a529f-138">INPUTS</span></span>

### <span data-ttu-id="a529f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a529f-139">System.String</span></span>

### <span data-ttu-id="a529f-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a529f-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a529f-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a529f-141">OUTPUTS</span></span>

### <span data-ttu-id="a529f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a529f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a529f-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a529f-143">NOTES</span></span>

## <span data-ttu-id="a529f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a529f-144">RELATED LINKS</span></span>

[<span data-ttu-id="a529f-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a529f-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="a529f-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a529f-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="a529f-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a529f-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="a529f-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a529f-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="a529f-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a529f-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
