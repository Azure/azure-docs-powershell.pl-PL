---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 41851c1492c3c14e3129ba04367580b09cf3ffb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891873"
---
# <span data-ttu-id="8847a-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="8847a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8847a-102">SYNOPSIS</span></span>
<span data-ttu-id="8847a-103">Tworzy miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8847a-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="8847a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8847a-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8847a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8847a-105">DESCRIPTION</span></span>
<span data-ttu-id="8847a-106">Polecenie cmdlet **New-AzWebAppSlot** tworzy miejsce w usłudze Azure Web App w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="8847a-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="8847a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8847a-107">EXAMPLES</span></span>

### <span data-ttu-id="8847a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8847a-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="8847a-109">To polecenie tworzy gniazdo o nazwie Slot001 w obszarze istniejących nazw aplikacji sieci Web ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-zachód w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="8847a-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="8847a-110">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="8847a-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="8847a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8847a-111">PARAMETERS</span></span>

### <span data-ttu-id="8847a-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8847a-112">-AppServicePlan</span></span>
<span data-ttu-id="8847a-113">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="8847a-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="8847a-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="8847a-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="8847a-115">Ustawienia aplikacji zastępuje obiekt Hashtable</span><span class="sxs-lookup"><span data-stu-id="8847a-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="8847a-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="8847a-116">-AseName</span></span>
<span data-ttu-id="8847a-117">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="8847a-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="8847a-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8847a-118">-AseResourceGroupName</span></span>
<span data-ttu-id="8847a-119">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="8847a-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8847a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8847a-120">-DefaultProfile</span></span>
<span data-ttu-id="8847a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8847a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8847a-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="8847a-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="8847a-123">Ignoruj niestandardowe opcje nazw hostów</span><span class="sxs-lookup"><span data-stu-id="8847a-123">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="8847a-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="8847a-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="8847a-125">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="8847a-125">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="8847a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8847a-126">-Name</span></span>
<span data-ttu-id="8847a-127">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="8847a-127">Webapp Name</span></span>

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

### <span data-ttu-id="8847a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8847a-128">-ResourceGroupName</span></span>
<span data-ttu-id="8847a-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8847a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="8847a-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="8847a-130">-Slot</span></span>
<span data-ttu-id="8847a-131">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="8847a-131">Webapp Slot Name</span></span>

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

### <span data-ttu-id="8847a-132">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="8847a-132">-SourceWebApp</span></span>
<span data-ttu-id="8847a-133">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="8847a-133">Source WebApp Object</span></span>

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

### <span data-ttu-id="8847a-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8847a-134">-AsJob</span></span>
<span data-ttu-id="8847a-135">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8847a-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8847a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8847a-136">CommonParameters</span></span>
<span data-ttu-id="8847a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8847a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8847a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8847a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8847a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8847a-139">INPUTS</span></span>

### <span data-ttu-id="8847a-140">Klienta</span><span class="sxs-lookup"><span data-stu-id="8847a-140">Site</span></span>
<span data-ttu-id="8847a-141">Parametr "SourceWebApp" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="8847a-141">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8847a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8847a-142">OUTPUTS</span></span>

## <span data-ttu-id="8847a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8847a-143">NOTES</span></span>

## <span data-ttu-id="8847a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8847a-144">RELATED LINKS</span></span>

[<span data-ttu-id="8847a-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8847a-146">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-146">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8847a-147">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-147">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8847a-148">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-148">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8847a-149">Start — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-149">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="8847a-150">Zatrzymaj — AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8847a-150">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8847a-151">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8847a-151">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="8847a-152">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8847a-152">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
