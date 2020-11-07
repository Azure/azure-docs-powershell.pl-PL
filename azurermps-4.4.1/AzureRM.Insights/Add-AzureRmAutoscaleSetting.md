---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719303"
---
# <span data-ttu-id="ca8ef-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca8ef-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="ca8ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8ef-103">Umożliwia utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca8ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca8ef-104">SYNTAX</span></span>

### <span data-ttu-id="ca8ef-105">Parametry polecenia cmdlet Add-AzureRmAutoscaleSetting w semantyce aktualizacji</span><span class="sxs-lookup"><span data-stu-id="ca8ef-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca8ef-106">Parametry polecenia cmdlet Add-AzureRmAutoscaleSetting w składni tworzenia semantyki</span><span class="sxs-lookup"><span data-stu-id="ca8ef-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca8ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ca8ef-107">DESCRIPTION</span></span>
<span data-ttu-id="ca8ef-108">Polecenie cmdlet **Add-AzureRmAutoscaleSetting** powoduje utworzenie ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="ca8ef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca8ef-109">EXAMPLES</span></span>

### <span data-ttu-id="ca8ef-110">Przykład 1. Tworzenie ustawienia skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="ca8ef-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="ca8ef-111">Dwa pierwsze polecenia używają New-AzureRmAutoscaleRule do tworzenia dwóch reguł autoskalowania $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="ca8ef-112">W przypadku trzeciego i czwartego polecenia za pomocą New-AzureRmAutoscaleProfile utworzyć profile skalowania automatycznego, $Profile 1 i $Profile 2, używając $Rule 1 i $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="ca8ef-113">Polecenie ostatnie powoduje utworzenie ustawienia skalowania automatycznego przy użyciu profilów w $Profile 1 i $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="ca8ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca8ef-114">PARAMETERS</span></span>

### <span data-ttu-id="ca8ef-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="ca8ef-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="ca8ef-116">Określa listę profilów, które mają zostać dodane do ustawienia skalowania automatycznego, lub $Null, aby dodać pozycję bez profilu.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="ca8ef-117">-DisableSetting</span></span>
<span data-ttu-id="ca8ef-118">Wyłącza istniejące ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-118">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca8ef-119">-Location</span></span>
<span data-ttu-id="ca8ef-120">Określa lokalizację ustawienia skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca8ef-121">-Name</span></span>
<span data-ttu-id="ca8ef-122">Określa nazwę ustawienia skalowania automatycznego, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-123">-Powiadomienia</span><span class="sxs-lookup"><span data-stu-id="ca8ef-123">-Notifications</span></span>
<span data-ttu-id="ca8ef-124">Określa listę oddzielonych przecinkami powiadomień.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-124">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ca8ef-125">-ResourceGroup</span></span>
<span data-ttu-id="ca8ef-126">Określa nazwę grupy zasobów dla zasobu skojarzonego z ustawieniem skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="ca8ef-127">-SettingSpec</span></span>
<span data-ttu-id="ca8ef-128">Określa obiekt **AutoscaleSetting** .</span><span class="sxs-lookup"><span data-stu-id="ca8ef-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="ca8ef-129">Za pomocą polecenia cmdlet Get-AzureRmAutoscaleSetting można uzyskać obiekt **AutoscaleSetting** lub utworzyć go w skrypcie programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8ef-130">-TargetResourceId</span></span>
<span data-ttu-id="ca8ef-131">Określa identyfikator zasobu do automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8ef-132">-DefaultProfile</span></span>
<span data-ttu-id="ca8ef-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca8ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8ef-134">CommonParameters</span></span>
<span data-ttu-id="ca8ef-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8ef-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca8ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8ef-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca8ef-137">INPUTS</span></span>

## <span data-ttu-id="ca8ef-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca8ef-138">OUTPUTS</span></span>

### <span data-ttu-id="ca8ef-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ca8ef-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="ca8ef-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca8ef-140">NOTES</span></span>

## <span data-ttu-id="ca8ef-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca8ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="ca8ef-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca8ef-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="ca8ef-143">Nowe — AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="ca8ef-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="ca8ef-144">Nowe — AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="ca8ef-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="ca8ef-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="ca8ef-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


