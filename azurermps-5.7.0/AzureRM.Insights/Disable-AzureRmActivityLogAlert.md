---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 3a78dd91879082c39ae8d7d737484d532ff63f7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549755"
---
# <span data-ttu-id="4d52a-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d52a-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="4d52a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d52a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d52a-103">Wyłącza alert dziennika aktywności i ustawia jego Tagi.</span><span class="sxs-lookup"><span data-stu-id="4d52a-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d52a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d52a-104">SYNTAX</span></span>

### <span data-ttu-id="4d52a-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d52a-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d52a-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d52a-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d52a-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d52a-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d52a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4d52a-108">DESCRIPTION</span></span>
<span data-ttu-id="4d52a-109">Polecenie cmdlet **disable-AzureRmActivityLogAlert** wyłącza alert dziennika aktywności i umożliwia ustawianie jego tagów.</span><span class="sxs-lookup"><span data-stu-id="4d52a-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="4d52a-110">To polecenie cmdlet implementuje wzorzec ShouldProcess, tzn. może zażądać potwierdzenia od użytkownika przed faktycznym zainstalowaniem zasobu.</span><span class="sxs-lookup"><span data-stu-id="4d52a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="4d52a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d52a-111">EXAMPLES</span></span>

### <span data-ttu-id="4d52a-112">Przykład 1. Wyłączanie alertu dziennika aktywności</span><span class="sxs-lookup"><span data-stu-id="4d52a-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="4d52a-113">To polecenie wyłącza alert dziennika aktywności o nazwie alert1 w grupie zasobów domyślna — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="4d52a-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="4d52a-114">To polecenie powoduje zmianę właściwości znaczników alertu dziennika aktywności o nazwie alert1 i wyłączenie go.</span><span class="sxs-lookup"><span data-stu-id="4d52a-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="4d52a-115">Przykład 2: wyłączanie alertu w dzienniku aktywności przy użyciu obiektu PSActivityLogAlertResource jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="4d52a-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="4d52a-116">To polecenie wyłącza alert dziennika aktywności o nazwie alert1.</span><span class="sxs-lookup"><span data-stu-id="4d52a-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="4d52a-117">W tym przypadku obiekt PSActivityLogAlertResource jest używany jako argument wejściowy.</span><span class="sxs-lookup"><span data-stu-id="4d52a-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="4d52a-118">Przykład 3: wyłączanie ActivityLogAlert przy użyciu parametru ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d52a-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="4d52a-119">To polecenie wyłącza ActivityLogAlert przy użyciu parametru ResourceId z potoku.</span><span class="sxs-lookup"><span data-stu-id="4d52a-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="4d52a-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d52a-120">PARAMETERS</span></span>

### <span data-ttu-id="4d52a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d52a-121">-DefaultProfile</span></span>
<span data-ttu-id="4d52a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4d52a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4d52a-123">-InputObject</span></span>
<span data-ttu-id="4d52a-124">Umożliwia ustawienie właściwości Inputobject dla połączenia w celu wyodrębnienia wymaganej nazwy, nazwy grupy zasobów i właściwości znacznika opcjonalnego.</span><span class="sxs-lookup"><span data-stu-id="4d52a-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d52a-125">-Name</span></span>
<span data-ttu-id="4d52a-126">Nazwa alertu dziennika aktywności.</span><span class="sxs-lookup"><span data-stu-id="4d52a-126">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d52a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d52a-128">Nazwa grupy zasobów, w której ma się znajdować zasób alertu.</span><span class="sxs-lookup"><span data-stu-id="4d52a-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d52a-129">-ResourceId</span></span>
<span data-ttu-id="4d52a-130">Ustawia właściwość znaczniki ResourceId połączenia, aby wyodrębnić wymaganą nazwę, właściwości nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4d52a-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: DisableByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d52a-131">-Confirm</span></span>
<span data-ttu-id="4d52a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d52a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d52a-133">-WhatIf</span></span>
<span data-ttu-id="4d52a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d52a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d52a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d52a-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d52a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d52a-136">CommonParameters</span></span>
<span data-ttu-id="4d52a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d52a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d52a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d52a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d52a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d52a-139">INPUTS</span></span>

### <span data-ttu-id="4d52a-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4d52a-140">None</span></span>
<span data-ttu-id="4d52a-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4d52a-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d52a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d52a-142">OUTPUTS</span></span>

### <span data-ttu-id="4d52a-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="4d52a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="4d52a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d52a-144">NOTES</span></span>

## <span data-ttu-id="4d52a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d52a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4d52a-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d52a-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4d52a-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d52a-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4d52a-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d52a-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4d52a-149">Nowe — AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4d52a-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="4d52a-150">Nowe — AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4d52a-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="4d52a-151">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4d52a-151">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
