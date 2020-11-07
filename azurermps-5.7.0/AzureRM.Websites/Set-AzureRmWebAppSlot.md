---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 717f355326acc4d169bee1e93d98446fa052a5e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718404"
---
# <span data-ttu-id="7baba-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="7baba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7baba-102">SYNOPSIS</span></span>
<span data-ttu-id="7baba-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7baba-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7baba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7baba-104">SYNTAX</span></span>

### <span data-ttu-id="7baba-105">S1</span><span class="sxs-lookup"><span data-stu-id="7baba-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7baba-106">S2</span><span class="sxs-lookup"><span data-stu-id="7baba-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7baba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7baba-107">DESCRIPTION</span></span>
<span data-ttu-id="7baba-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7baba-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="7baba-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7baba-109">EXAMPLES</span></span>

### <span data-ttu-id="7baba-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7baba-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="7baba-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="7baba-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7baba-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7baba-112">PARAMETERS</span></span>

### <span data-ttu-id="7baba-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7baba-113">-AppServicePlan</span></span>
<span data-ttu-id="7baba-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="7baba-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="7baba-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="7baba-115">-AppSettings</span></span>
<span data-ttu-id="7baba-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="7baba-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="7baba-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="7baba-118">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="7baba-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="7baba-119">-ConnectionStrings</span></span>
<span data-ttu-id="7baba-120">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="7baba-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="7baba-121">-DefaultDocuments</span></span>
<span data-ttu-id="7baba-122">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="7baba-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baba-123">-DefaultProfile</span></span>
<span data-ttu-id="7baba-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7baba-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7baba-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7baba-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="7baba-126">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="7baba-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="7baba-127">-HandlerMappings</span></span>
<span data-ttu-id="7baba-128">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="7baba-128">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7baba-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="7baba-130">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7baba-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="7baba-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="7baba-132">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="7baba-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7baba-133">-Name</span></span>
<span data-ttu-id="7baba-134">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="7baba-134">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="7baba-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="7baba-136">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="7baba-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="7baba-137">-NumberOfWorkers</span></span>
<span data-ttu-id="7baba-138">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="7baba-138">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="7baba-139">-PhpVersion</span></span>
<span data-ttu-id="7baba-140">Wersja php</span><span class="sxs-lookup"><span data-stu-id="7baba-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="7baba-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="7baba-142">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="7baba-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7baba-143">-ResourceGroupName</span></span>
<span data-ttu-id="7baba-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7baba-144">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="7baba-145">-Slot</span></span>
<span data-ttu-id="7baba-146">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="7baba-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="7baba-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="7baba-148">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="7baba-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-149">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="7baba-149">-WebApp</span></span>
<span data-ttu-id="7baba-150">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="7baba-150">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7baba-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="7baba-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="7baba-152">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="7baba-152">Web Sockets Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="7baba-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7baba-153">-AsJob</span></span>
<span data-ttu-id="7baba-154">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7baba-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7baba-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baba-155">CommonParameters</span></span>
<span data-ttu-id="7baba-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7baba-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baba-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baba-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baba-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7baba-158">INPUTS</span></span>

### <span data-ttu-id="7baba-159">Elementem</span><span class="sxs-lookup"><span data-stu-id="7baba-159">Int32</span></span>
<span data-ttu-id="7baba-160">Parametr "NumberOfWorkers" akceptuje wartość typu "Int32" z procesu</span><span class="sxs-lookup"><span data-stu-id="7baba-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="7baba-161">Klienta</span><span class="sxs-lookup"><span data-stu-id="7baba-161">Site</span></span>
<span data-ttu-id="7baba-162">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="7baba-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7baba-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7baba-163">OUTPUTS</span></span>

## <span data-ttu-id="7baba-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7baba-164">NOTES</span></span>

## <span data-ttu-id="7baba-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7baba-165">RELATED LINKS</span></span>

[<span data-ttu-id="7baba-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-167">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-167">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-168">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-168">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-169">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-169">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-170">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-170">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-171">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7baba-171">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="7baba-172">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7baba-172">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
