---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203532"
---
# <span data-ttu-id="cf794-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cf794-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="cf794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf794-102">SYNOPSIS</span></span>
<span data-ttu-id="cf794-103">Wyłącza alert dziennika aktywności i ustawia jego tagi.</span><span class="sxs-lookup"><span data-stu-id="cf794-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="cf794-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf794-104">SYNTAX</span></span>

### <span data-ttu-id="cf794-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cf794-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf794-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf794-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf794-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf794-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf794-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf794-108">DESCRIPTION</span></span>
<span data-ttu-id="cf794-109">Polecenie **cmdlet Disable-AzActivityLogAlert** wyłącza alert dziennika aktywności i umożliwia ustawianie tagów.</span><span class="sxs-lookup"><span data-stu-id="cf794-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="cf794-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, czyli może wymagać potwierdzenia od użytkownika przed wykonaniem poprawek dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="cf794-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="cf794-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf794-111">EXAMPLES</span></span>

### <span data-ttu-id="cf794-112">Przykład 1. Wyłączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="cf794-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="cf794-113">To polecenie wyłącza alert dziennika aktywności o nazwie alert1 w grupie zasobów Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="cf794-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="cf794-114">To polecenie zmienia właściwość tagów alertu dziennika aktywności nazywanego alertem1 i wyłącza go.</span><span class="sxs-lookup"><span data-stu-id="cf794-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="cf794-115">Przykład 2. Wyłączanie alertu dziennika aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="cf794-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="cf794-116">To polecenie wyłącza alert dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="cf794-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="cf794-117">W tym celu jako argument wejściowy jest używany obiekt PSActivityLogAlertResource.</span><span class="sxs-lookup"><span data-stu-id="cf794-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="cf794-118">Przykład 3. Wyłączanie parametru ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf794-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="cf794-119">To polecenie wyłącza parametr ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="cf794-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="cf794-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf794-120">PARAMETERS</span></span>

### <span data-ttu-id="cf794-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf794-121">-DefaultProfile</span></span>
<span data-ttu-id="cf794-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cf794-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf794-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf794-123">-InputObject</span></span>
<span data-ttu-id="cf794-124">Ustawia właściwość tagów InputObject połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i opcjonalnych właściwości tagu.</span><span class="sxs-lookup"><span data-stu-id="cf794-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf794-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf794-125">-Name</span></span>
<span data-ttu-id="cf794-126">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="cf794-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf794-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf794-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf794-128">Nazwa grupy zasobów, w której ma istnieć zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="cf794-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf794-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf794-129">-ResourceId</span></span>
<span data-ttu-id="cf794-130">Ustawia właściwość tagów ResourceId połączenia w celu wyodrębnienia wymaganej nazwy, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf794-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf794-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf794-131">-Confirm</span></span>
<span data-ttu-id="cf794-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cf794-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf794-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf794-133">-WhatIf</span></span>
<span data-ttu-id="cf794-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf794-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf794-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cf794-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf794-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf794-136">CommonParameters</span></span>
<span data-ttu-id="cf794-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf794-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf794-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf794-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf794-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf794-139">INPUTS</span></span>

### <span data-ttu-id="cf794-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cf794-140">System.String</span></span>

### <span data-ttu-id="cf794-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="cf794-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="cf794-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf794-142">OUTPUTS</span></span>

### <span data-ttu-id="cf794-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="cf794-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="cf794-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf794-144">NOTES</span></span>

## <span data-ttu-id="cf794-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf794-145">RELATED LINKS</span></span>

[<span data-ttu-id="cf794-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cf794-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="cf794-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cf794-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="cf794-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cf794-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="cf794-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="cf794-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="cf794-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="cf794-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="cf794-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cf794-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
