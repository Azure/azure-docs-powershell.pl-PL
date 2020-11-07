---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719644"
---
# <span data-ttu-id="b05c8-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b05c8-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="b05c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b05c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b05c8-103">Usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="b05c8-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b05c8-104">SYNTAX</span></span>

### <span data-ttu-id="b05c8-105">Domyślne parametry usuwania alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="b05c8-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b05c8-106">Parametry usuwania alertów dziennika aktywności z przeprowadzoną wartością z potoku</span><span class="sxs-lookup"><span data-stu-id="b05c8-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b05c8-107">Parametry usuwania alertów dziennika aktywności przyjmujących wartość ResourceId z potoku</span><span class="sxs-lookup"><span data-stu-id="b05c8-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b05c8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b05c8-108">DESCRIPTION</span></span>
<span data-ttu-id="b05c8-109">Polecenie cmdlet **Remove-AzureRmActivityLogAlert** usuwa alert dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="b05c8-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="b05c8-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="b05c8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="b05c8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b05c8-111">EXAMPLES</span></span>

### <span data-ttu-id="b05c8-112">Przykład 1: Usuwanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="b05c8-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="b05c8-113">Usuwa alert dziennika aktywności przy użyciu nazw i grup zasobów jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b05c8-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="b05c8-114">Przykład 2: Usuwanie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="b05c8-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="b05c8-115">Umożliwia usunięcie alertu dziennika aktywności przy użyciu PSActivityLogAlertResource jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b05c8-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="b05c8-116">Przykład 3: usuwanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="b05c8-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="b05c8-117">To polecenie usuwa ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="b05c8-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="b05c8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b05c8-118">PARAMETERS</span></span>

### <span data-ttu-id="b05c8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b05c8-119">-Name</span></span>
<span data-ttu-id="b05c8-120">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="b05c8-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05c8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b05c8-121">-ResourceGroupName</span></span>
<span data-ttu-id="b05c8-122">Nazwa grupy zasobów, w której znajduje się zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="b05c8-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05c8-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b05c8-123">-InputObject</span></span>
<span data-ttu-id="b05c8-124">Ustawia właściwość Inputobject dla połączenia, aby wyodrębnić nazwę wymaganą, oraz właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b05c8-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b05c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b05c8-125">-ResourceId</span></span>
<span data-ttu-id="b05c8-126">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b05c8-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b05c8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b05c8-127">-Confirm</span></span>
<span data-ttu-id="b05c8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b05c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b05c8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05c8-129">-DefaultProfile</span></span>
<span data-ttu-id="b05c8-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b05c8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b05c8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b05c8-131">-WhatIf</span></span>
<span data-ttu-id="b05c8-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b05c8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b05c8-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b05c8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b05c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05c8-134">CommonParameters</span></span>
<span data-ttu-id="b05c8-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b05c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05c8-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05c8-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b05c8-137">INPUTS</span></span>

## <span data-ttu-id="b05c8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b05c8-138">OUTPUTS</span></span>

### <span data-ttu-id="b05c8-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b05c8-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="b05c8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b05c8-140">NOTES</span></span>

## <span data-ttu-id="b05c8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b05c8-141">RELATED LINKS</span></span>

[<span data-ttu-id="b05c8-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b05c8-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b05c8-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b05c8-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b05c8-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b05c8-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b05c8-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b05c8-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b05c8-146">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b05c8-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="b05c8-147">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b05c8-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

