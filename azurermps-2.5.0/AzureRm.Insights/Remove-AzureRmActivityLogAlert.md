---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898474"
---
# <span data-ttu-id="e7587-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7587-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="e7587-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7587-102">SYNOPSIS</span></span>
<span data-ttu-id="e7587-103">Usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="e7587-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7587-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7587-104">SYNTAX</span></span>

### <span data-ttu-id="e7587-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e7587-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7587-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7587-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7587-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7587-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7587-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e7587-108">DESCRIPTION</span></span>
<span data-ttu-id="e7587-109">Polecenie cmdlet **Remove-AzureRmActivityLogAlert** usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="e7587-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="e7587-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7587-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="e7587-111">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym utworzeniem, zmodyfikowaniem lub usunięciem zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7587-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e7587-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7587-112">EXAMPLES</span></span>

### <span data-ttu-id="e7587-113">Przykład 1: Usuwanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="e7587-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="e7587-114">Usuwa alert dziennika aktywności przy użyciu nazw i grup zasobów jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e7587-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="e7587-115">Przykład 2: Usuwanie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="e7587-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="e7587-116">Umożliwia usunięcie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e7587-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="e7587-117">Przykład 3: usuwanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7587-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="e7587-118">To polecenie usuwa ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="e7587-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e7587-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7587-119">PARAMETERS</span></span>

### <span data-ttu-id="e7587-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7587-120">-DefaultProfile</span></span>
<span data-ttu-id="e7587-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e7587-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7587-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e7587-122">-InputObject</span></span>
<span data-ttu-id="e7587-123">Ustawia właściwość Inputobject dla połączenia, aby wyodrębnić nazwę wymaganą, oraz właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7587-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7587-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7587-124">-Name</span></span>
<span data-ttu-id="e7587-125">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="e7587-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7587-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7587-126">-ResourceGroupName</span></span>
<span data-ttu-id="e7587-127">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="e7587-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7587-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7587-128">-ResourceId</span></span>
<span data-ttu-id="e7587-129">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7587-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7587-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7587-130">-Confirm</span></span>
<span data-ttu-id="e7587-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7587-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7587-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7587-132">-WhatIf</span></span>
<span data-ttu-id="e7587-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7587-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7587-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7587-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7587-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7587-135">CommonParameters</span></span>
<span data-ttu-id="e7587-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7587-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7587-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7587-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7587-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7587-138">INPUTS</span></span>

### <span data-ttu-id="e7587-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e7587-139">System.String</span></span>

### <span data-ttu-id="e7587-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e7587-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="e7587-141">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7587-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e7587-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7587-142">OUTPUTS</span></span>

### <span data-ttu-id="e7587-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7587-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e7587-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7587-144">NOTES</span></span>

## <span data-ttu-id="e7587-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7587-145">RELATED LINKS</span></span>

[<span data-ttu-id="e7587-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7587-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e7587-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7587-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e7587-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7587-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e7587-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7587-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e7587-150">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e7587-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="e7587-151">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e7587-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

