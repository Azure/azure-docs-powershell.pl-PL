---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222459"
---
# <span data-ttu-id="a02d4-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a02d4-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="a02d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a02d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a02d4-103">Włącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="a02d4-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="a02d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a02d4-104">SYNTAX</span></span>

### <span data-ttu-id="a02d4-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a02d4-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02d4-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="a02d4-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02d4-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="a02d4-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a02d4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a02d4-108">DESCRIPTION</span></span>
<span data-ttu-id="a02d4-109">Polecenie cmdlet **enable-AzActivityLogAlert** umożliwia włączenie alertu dziennika aktywności i ustawienie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="a02d4-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="a02d4-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="a02d4-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a02d4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a02d4-111">EXAMPLES</span></span>

### <span data-ttu-id="a02d4-112">Przykład 1. Włączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="a02d4-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a02d4-113">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1 w grupie zasobów domyślne — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="a02d4-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="a02d4-114">Przykład 2: Włączanie alertu dziennika aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="a02d4-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a02d4-115">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="a02d4-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="a02d4-116">W tym przypadku obiekt PSActivityLogAlertResource jest używany jako argument wejściowy.</span><span class="sxs-lookup"><span data-stu-id="a02d4-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a02d4-117">Przykład 3: Włączanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02d4-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="a02d4-118">To polecenie włącza ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="a02d4-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a02d4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a02d4-119">PARAMETERS</span></span>

### <span data-ttu-id="a02d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02d4-120">-DefaultProfile</span></span>
<span data-ttu-id="a02d4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a02d4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a02d4-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a02d4-122">-InputObject</span></span>
<span data-ttu-id="a02d4-123">Umożliwia ustawienie właściwości Inputobject dla połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i właściwości znaczników opcjonalnych.</span><span class="sxs-lookup"><span data-stu-id="a02d4-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="a02d4-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a02d4-124">-Name</span></span>
<span data-ttu-id="a02d4-125">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="a02d4-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="a02d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="a02d4-127">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="a02d4-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="a02d4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02d4-128">-ResourceId</span></span>
<span data-ttu-id="a02d4-129">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a02d4-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="a02d4-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a02d4-130">-Confirm</span></span>
<span data-ttu-id="a02d4-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a02d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a02d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a02d4-132">-WhatIf</span></span>
<span data-ttu-id="a02d4-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a02d4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a02d4-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a02d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a02d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02d4-135">CommonParameters</span></span>
<span data-ttu-id="a02d4-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02d4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a02d4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02d4-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a02d4-138">INPUTS</span></span>

### <span data-ttu-id="a02d4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a02d4-139">System.String</span></span>

### <span data-ttu-id="a02d4-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a02d4-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a02d4-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a02d4-141">OUTPUTS</span></span>

### <span data-ttu-id="a02d4-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a02d4-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a02d4-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a02d4-143">NOTES</span></span>

## <span data-ttu-id="a02d4-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a02d4-144">RELATED LINKS</span></span>

[<span data-ttu-id="a02d4-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a02d4-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="a02d4-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a02d4-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="a02d4-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a02d4-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="a02d4-148">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a02d4-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="a02d4-149">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a02d4-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="a02d4-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a02d4-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
