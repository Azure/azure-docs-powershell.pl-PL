---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 84a377e2936a2c9f5aeaf0516dc96f848b9eb0b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891233"
---
# <span data-ttu-id="2e8a5-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e8a5-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="2e8a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8a5-103">Wyłącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="2e8a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e8a5-104">SYNTAX</span></span>

### <span data-ttu-id="2e8a5-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2e8a5-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e8a5-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e8a5-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e8a5-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="2e8a5-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e8a5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2e8a5-108">DESCRIPTION</span></span>
<span data-ttu-id="2e8a5-109">Polecenie cmdlet **disable-AzActivityLogAlert** wyłącza alert dziennika aktywności i umożliwia ustawianie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="2e8a5-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="2e8a5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e8a5-111">EXAMPLES</span></span>

### <span data-ttu-id="2e8a5-112">Przykład 1. Wyłączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="2e8a5-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="2e8a5-113">To polecenie wyłącza alert dziennika aktywności o nazwie alert1 w grupie zasobów domyślna — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="2e8a5-114">To polecenie powoduje zmianę właściwości znaczników alertu dziennika aktywności o nazwie alert1 i wyłączenie go.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="2e8a5-115">Przykład 2: wyłączanie alertu w dzienniku aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="2e8a5-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="2e8a5-116">To polecenie wyłącza alert dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="2e8a5-117">W tym przypadku obiekt PSActivityLogAlertResource jest używany jako argument wejściowy.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="2e8a5-118">Przykład 3: wyłączanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e8a5-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="2e8a5-119">To polecenie wyłącza ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="2e8a5-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e8a5-120">PARAMETERS</span></span>

### <span data-ttu-id="2e8a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8a5-121">-DefaultProfile</span></span>
<span data-ttu-id="2e8a5-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e8a5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e8a5-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e8a5-123">-InputObject</span></span>
<span data-ttu-id="2e8a5-124">Umożliwia ustawienie właściwości Inputobject dla połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i właściwości znacznika opcjonalnego.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="2e8a5-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e8a5-125">-Name</span></span>
<span data-ttu-id="2e8a5-126">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="2e8a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e8a5-128">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="2e8a5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e8a5-129">-ResourceId</span></span>
<span data-ttu-id="2e8a5-130">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="2e8a5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e8a5-131">-Confirm</span></span>
<span data-ttu-id="2e8a5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8a5-133">-WhatIf</span></span>
<span data-ttu-id="2e8a5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e8a5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8a5-136">CommonParameters</span></span>
<span data-ttu-id="2e8a5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8a5-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e8a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8a5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e8a5-139">INPUTS</span></span>

### <span data-ttu-id="2e8a5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2e8a5-140">System.String</span></span>

### <span data-ttu-id="2e8a5-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2e8a5-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2e8a5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e8a5-142">OUTPUTS</span></span>

### <span data-ttu-id="2e8a5-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2e8a5-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2e8a5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e8a5-144">NOTES</span></span>

## <span data-ttu-id="2e8a5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e8a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="2e8a5-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e8a5-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2e8a5-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e8a5-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="2e8a5-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e8a5-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2e8a5-149">Nowe — AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2e8a5-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="2e8a5-150">Nowe — AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2e8a5-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="2e8a5-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2e8a5-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
