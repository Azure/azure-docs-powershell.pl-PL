---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898121"
---
# <span data-ttu-id="47caa-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="47caa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47caa-102">SYNOPSIS</span></span>
<span data-ttu-id="47caa-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="47caa-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47caa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47caa-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47caa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47caa-105">DESCRIPTION</span></span>
<span data-ttu-id="47caa-106">Polecenie cmdlet **New-AzureRmWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="47caa-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="47caa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47caa-107">EXAMPLES</span></span>

### <span data-ttu-id="47caa-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="47caa-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="47caa-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="47caa-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="47caa-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="47caa-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="47caa-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47caa-111">PARAMETERS</span></span>

### <span data-ttu-id="47caa-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="47caa-112">-AppServicePlan</span></span>
<span data-ttu-id="47caa-113">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="47caa-113">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="47caa-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="47caa-115">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="47caa-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="47caa-116">-AseName</span></span>
<span data-ttu-id="47caa-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="47caa-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47caa-118">-AseResourceGroupName</span></span>
<span data-ttu-id="47caa-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="47caa-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47caa-120">-DefaultProfile</span></span>
<span data-ttu-id="47caa-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47caa-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47caa-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="47caa-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="47caa-123">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="47caa-123">Ignore Custom HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="47caa-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="47caa-125">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="47caa-125">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="47caa-126">-Name</span></span>
<span data-ttu-id="47caa-127">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="47caa-127">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47caa-128">-ResourceGroupName</span></span>
<span data-ttu-id="47caa-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="47caa-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="47caa-130">-Slot</span></span>
<span data-ttu-id="47caa-131">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="47caa-131">Webapp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="47caa-132">-SourceWebApp</span></span>
<span data-ttu-id="47caa-133">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="47caa-133">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47caa-134">-AsJob</span></span>
<span data-ttu-id="47caa-135">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="47caa-135">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47caa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47caa-136">CommonParameters</span></span>
<span data-ttu-id="47caa-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47caa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47caa-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47caa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47caa-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47caa-139">INPUTS</span></span>

### <span data-ttu-id="47caa-140">Klienta</span><span class="sxs-lookup"><span data-stu-id="47caa-140">Site</span></span>
<span data-ttu-id="47caa-141">Parametr "SourceWebApp" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="47caa-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="47caa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47caa-142">OUTPUTS</span></span>

## <span data-ttu-id="47caa-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47caa-143">NOTES</span></span>

## <span data-ttu-id="47caa-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47caa-144">RELATED LINKS</span></span>

[<span data-ttu-id="47caa-145">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-145">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-146">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-146">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-147">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-147">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-148">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-148">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-149">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-149">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-150">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47caa-150">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="47caa-151">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="47caa-151">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="47caa-152">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="47caa-152">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
