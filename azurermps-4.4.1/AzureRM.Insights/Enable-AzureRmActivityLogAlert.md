---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553866"
---
# <span data-ttu-id="43fb9-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="43fb9-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="43fb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="43fb9-103">Włącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="43fb9-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43fb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43fb9-104">SYNTAX</span></span>

### <span data-ttu-id="43fb9-105">Domyślne parametry włączania alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="43fb9-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43fb9-106">Parametry umożliwiające włączenie alertów dotyczących dziennika aktywności z przeprowadzoną wartością z potoku</span><span class="sxs-lookup"><span data-stu-id="43fb9-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43fb9-107">Parametry w celu włączenia alertów dotyczących dziennika aktywności przyjmujących wartość ResourceId z potoku</span><span class="sxs-lookup"><span data-stu-id="43fb9-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43fb9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="43fb9-108">DESCRIPTION</span></span>
<span data-ttu-id="43fb9-109">Polecenie cmdlet **enable-AzureRmActivityLogAlert** umożliwia włączenie alertu dziennika aktywności i ustawienie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="43fb9-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="43fb9-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="43fb9-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="43fb9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43fb9-111">EXAMPLES</span></span>

### <span data-ttu-id="43fb9-112">Przykład 1. Wyłączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="43fb9-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="43fb9-113">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1 w grupie zasobów domyślne — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="43fb9-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="43fb9-114">Przykład 2: Włączanie alertu dziennika aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="43fb9-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="43fb9-115">To polecenie umożliwia włączenie alertu dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="43fb9-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="43fb9-116">W tym przypadku obiekt PSActivityLogAlertResource jest używany jako argument wejściowy.</span><span class="sxs-lookup"><span data-stu-id="43fb9-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="43fb9-117">Przykład 3: Włączanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="43fb9-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="43fb9-118">To polecenie włącza ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="43fb9-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="43fb9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43fb9-119">PARAMETERS</span></span>

### <span data-ttu-id="43fb9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="43fb9-120">-Name</span></span>
<span data-ttu-id="43fb9-121">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="43fb9-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43fb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="43fb9-123">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="43fb9-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43fb9-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43fb9-124">-InputObject</span></span>
<span data-ttu-id="43fb9-125">Umożliwia ustawienie właściwości Inputobject dla połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i właściwości znaczników opcjonalnych.</span><span class="sxs-lookup"><span data-stu-id="43fb9-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43fb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43fb9-126">-ResourceId</span></span>
<span data-ttu-id="43fb9-127">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43fb9-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43fb9-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43fb9-128">-Confirm</span></span>
<span data-ttu-id="43fb9-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43fb9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43fb9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fb9-130">-DefaultProfile</span></span>
<span data-ttu-id="43fb9-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43fb9-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43fb9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43fb9-132">-WhatIf</span></span>
<span data-ttu-id="43fb9-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43fb9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43fb9-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43fb9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43fb9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fb9-135">CommonParameters</span></span>
<span data-ttu-id="43fb9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fb9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fb9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43fb9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fb9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43fb9-138">INPUTS</span></span>

## <span data-ttu-id="43fb9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43fb9-139">OUTPUTS</span></span>

### <span data-ttu-id="43fb9-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="43fb9-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="43fb9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43fb9-141">NOTES</span></span>

## <span data-ttu-id="43fb9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43fb9-142">RELATED LINKS</span></span>

[<span data-ttu-id="43fb9-143">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="43fb9-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="43fb9-144">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="43fb9-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="43fb9-145">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="43fb9-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="43fb9-146">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="43fb9-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="43fb9-147">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="43fb9-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="43fb9-148">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="43fb9-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
