---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 856e3abc5cf99c7ae7f871619476717af21aed9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899343"
---
# <span data-ttu-id="e0e36-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0e36-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="e0e36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0e36-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e36-103">Włącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="e0e36-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0e36-104">SYNTAX</span></span>

### <span data-ttu-id="e0e36-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0e36-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e36-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0e36-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0e36-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e36-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e36-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e0e36-108">DESCRIPTION</span></span>
<span data-ttu-id="e0e36-109">Polecenie cmdlet **enable-AzureRmActivityLogAlert** umożliwia włączenie alertu dziennika aktywności i ustawienie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="e0e36-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="e0e36-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="e0e36-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="e0e36-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0e36-111">EXAMPLES</span></span>

### <span data-ttu-id="e0e36-112">Przykład 1. Wyłączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="e0e36-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="e0e36-113">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1 w grupie zasobów domyślne — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="e0e36-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="e0e36-114">Przykład 2: Włączanie alertu dziennika aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="e0e36-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="e0e36-115">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="e0e36-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="e0e36-116">W tym przypadku obiekt PSActivityLogAlertResource jest używany jako argument wejściowy.</span><span class="sxs-lookup"><span data-stu-id="e0e36-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="e0e36-117">Przykład 3: Włączanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e36-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="e0e36-118">To polecenie włącza ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="e0e36-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e0e36-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0e36-119">PARAMETERS</span></span>

### <span data-ttu-id="e0e36-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e36-120">-DefaultProfile</span></span>
<span data-ttu-id="e0e36-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e0e36-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e36-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e0e36-122">-InputObject</span></span>
<span data-ttu-id="e0e36-123">Umożliwia ustawienie właściwości Inputobject dla połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i właściwości znaczników opcjonalnych.</span><span class="sxs-lookup"><span data-stu-id="e0e36-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="e0e36-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0e36-124">-Name</span></span>
<span data-ttu-id="e0e36-125">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="e0e36-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="e0e36-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e36-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0e36-127">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="e0e36-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="e0e36-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0e36-128">-ResourceId</span></span>
<span data-ttu-id="e0e36-129">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0e36-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="e0e36-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0e36-130">-Confirm</span></span>
<span data-ttu-id="e0e36-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e36-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e36-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e36-132">-WhatIf</span></span>
<span data-ttu-id="e0e36-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e36-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0e36-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0e36-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e36-135">CommonParameters</span></span>
<span data-ttu-id="e0e36-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e36-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e36-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e36-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0e36-138">INPUTS</span></span>

### <span data-ttu-id="e0e36-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e0e36-139">System.String</span></span>

### <span data-ttu-id="e0e36-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e0e36-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="e0e36-141">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e0e36-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e0e36-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0e36-142">OUTPUTS</span></span>

### <span data-ttu-id="e0e36-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e0e36-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e0e36-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0e36-144">NOTES</span></span>

## <span data-ttu-id="e0e36-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0e36-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0e36-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0e36-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e0e36-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0e36-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e0e36-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0e36-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e0e36-149">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e0e36-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="e0e36-150">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e0e36-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="e0e36-151">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0e36-151">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
