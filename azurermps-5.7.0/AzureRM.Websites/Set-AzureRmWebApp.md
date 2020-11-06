---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551456"
---
# <span data-ttu-id="b2eb5-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="b2eb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b2eb5-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2eb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2eb5-104">SYNTAX</span></span>

### <span data-ttu-id="b2eb5-105">S1</span><span class="sxs-lookup"><span data-stu-id="b2eb5-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2eb5-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2eb5-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2eb5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b2eb5-107">DESCRIPTION</span></span>
<span data-ttu-id="b2eb5-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="b2eb5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2eb5-109">EXAMPLES</span></span>

### <span data-ttu-id="b2eb5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2eb5-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="b2eb5-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b2eb5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2eb5-112">PARAMETERS</span></span>

### <span data-ttu-id="b2eb5-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2eb5-113">-AppServicePlan</span></span>
<span data-ttu-id="b2eb5-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b2eb5-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="b2eb5-115">-AppSettings</span></span>
<span data-ttu-id="b2eb5-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2eb5-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="b2eb5-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="b2eb5-118">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="b2eb5-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b2eb5-119">-ConnectionStrings</span></span>
<span data-ttu-id="b2eb5-120">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="b2eb5-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="b2eb5-121">-DefaultDocuments</span></span>
<span data-ttu-id="b2eb5-122">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="b2eb5-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2eb5-123">-DefaultProfile</span></span>
<span data-ttu-id="b2eb5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2eb5-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="b2eb5-126">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="b2eb5-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="b2eb5-127">-HandlerMappings</span></span>
<span data-ttu-id="b2eb5-128">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="b2eb5-128">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-129">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="b2eb5-129">-HostNames</span></span>
<span data-ttu-id="b2eb5-130">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2eb5-130">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="b2eb5-132">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-132">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="b2eb5-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="b2eb5-134">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="b2eb5-134">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2eb5-135">-Name</span></span>
<span data-ttu-id="b2eb5-136">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2eb5-136">WebApp Name</span></span>

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

### <span data-ttu-id="b2eb5-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="b2eb5-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="b2eb5-138">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="b2eb5-138">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="b2eb5-139">-NumberOfWorkers</span></span>
<span data-ttu-id="b2eb5-140">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="b2eb5-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="b2eb5-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="b2eb5-141">-PhpVersion</span></span>
<span data-ttu-id="b2eb5-142">Wersja php</span><span class="sxs-lookup"><span data-stu-id="b2eb5-142">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="b2eb5-144">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="b2eb5-144">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2eb5-145">-ResourceGroupName</span></span>
<span data-ttu-id="b2eb5-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b2eb5-146">Resource Group Name</span></span>

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

### <span data-ttu-id="b2eb5-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="b2eb5-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="b2eb5-148">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="b2eb5-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="b2eb5-149">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2eb5-149">-WebApp</span></span>
<span data-ttu-id="b2eb5-150">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2eb5-150">WebApp Object</span></span>

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

### <span data-ttu-id="b2eb5-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="b2eb5-152">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b2eb5-152">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2eb5-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2eb5-153">-AsJob</span></span>
<span data-ttu-id="b2eb5-154">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2eb5-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2eb5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2eb5-155">CommonParameters</span></span>
<span data-ttu-id="b2eb5-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2eb5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2eb5-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2eb5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2eb5-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2eb5-158">INPUTS</span></span>

### <span data-ttu-id="b2eb5-159">Elementem</span><span class="sxs-lookup"><span data-stu-id="b2eb5-159">Int32</span></span>
<span data-ttu-id="b2eb5-160">Parametr "NumberOfWorkers" akceptuje wartość typu "Int32" z procesu</span><span class="sxs-lookup"><span data-stu-id="b2eb5-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="b2eb5-161">Klienta</span><span class="sxs-lookup"><span data-stu-id="b2eb5-161">Site</span></span>
<span data-ttu-id="b2eb5-162">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="b2eb5-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b2eb5-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2eb5-163">OUTPUTS</span></span>

## <span data-ttu-id="b2eb5-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2eb5-164">NOTES</span></span>

## <span data-ttu-id="b2eb5-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2eb5-165">RELATED LINKS</span></span>

[<span data-ttu-id="b2eb5-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="b2eb5-167">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="b2eb5-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="b2eb5-169">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="b2eb5-170">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="b2eb5-171">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="b2eb5-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
