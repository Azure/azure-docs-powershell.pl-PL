---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891833"
---
# <span data-ttu-id="b35c8-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-101">Set-AzWebApp</span></span>

## <span data-ttu-id="b35c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b35c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b35c8-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b35c8-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="b35c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b35c8-104">SYNTAX</span></span>

### <span data-ttu-id="b35c8-105">S1</span><span class="sxs-lookup"><span data-stu-id="b35c8-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b35c8-106">S2</span><span class="sxs-lookup"><span data-stu-id="b35c8-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b35c8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b35c8-107">DESCRIPTION</span></span>
<span data-ttu-id="b35c8-108">Polecenie cmdlet **Set-AzWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b35c8-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="b35c8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b35c8-109">EXAMPLES</span></span>

### <span data-ttu-id="b35c8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b35c8-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="b35c8-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="b35c8-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b35c8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b35c8-112">PARAMETERS</span></span>

### <span data-ttu-id="b35c8-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b35c8-113">-AppServicePlan</span></span>
<span data-ttu-id="b35c8-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="b35c8-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="b35c8-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="b35c8-115">-AppSettings</span></span>
<span data-ttu-id="b35c8-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="b35c8-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="b35c8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b35c8-117">-AsJob</span></span>
<span data-ttu-id="b35c8-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b35c8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b35c8-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b35c8-119">-AssignIdentity</span></span>
<span data-ttu-id="b35c8-120">Włączanie/wyłączanie Instalatora MSI na istniejącym platformie Azure aplikacji lub functionapp [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="b35c8-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c8-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="b35c8-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="b35c8-122">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="b35c8-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="b35c8-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b35c8-123">-ConnectionStrings</span></span>
<span data-ttu-id="b35c8-124">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="b35c8-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="b35c8-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="b35c8-125">-DefaultDocuments</span></span>
<span data-ttu-id="b35c8-126">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="b35c8-126">Default Documents String Array</span></span>

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

### <span data-ttu-id="b35c8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35c8-127">-DefaultProfile</span></span>
<span data-ttu-id="b35c8-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b35c8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b35c8-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="b35c8-130">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="b35c8-130">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="b35c8-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="b35c8-131">-HandlerMappings</span></span>
<span data-ttu-id="b35c8-132">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="b35c8-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="b35c8-133">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="b35c8-133">-HostNames</span></span>
<span data-ttu-id="b35c8-134">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="b35c8-134">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="b35c8-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="b35c8-136">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-136">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="b35c8-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b35c8-137">-HttpsOnly</span></span>
<span data-ttu-id="b35c8-138">Włączanie/wyłączanie przekierowywania całego ruchu do protokołu HTTPS na istniejącym platformie Azure aplikacji lub functionapp</span><span class="sxs-lookup"><span data-stu-id="b35c8-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b35c8-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="b35c8-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="b35c8-140">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="b35c8-140">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="b35c8-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b35c8-141">-Name</span></span>
<span data-ttu-id="b35c8-142">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b35c8-142">WebApp Name</span></span>

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

### <span data-ttu-id="b35c8-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="b35c8-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="b35c8-144">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="b35c8-144">Net Framework Version</span></span>

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

### <span data-ttu-id="b35c8-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="b35c8-145">-NumberOfWorkers</span></span>
<span data-ttu-id="b35c8-146">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="b35c8-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="b35c8-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="b35c8-147">-PhpVersion</span></span>
<span data-ttu-id="b35c8-148">Wersja php</span><span class="sxs-lookup"><span data-stu-id="b35c8-148">Php Version</span></span>

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

### <span data-ttu-id="b35c8-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="b35c8-150">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="b35c8-150">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="b35c8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b35c8-151">-ResourceGroupName</span></span>
<span data-ttu-id="b35c8-152">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b35c8-152">Resource Group Name</span></span>

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

### <span data-ttu-id="b35c8-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="b35c8-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="b35c8-154">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="b35c8-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="b35c8-155">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="b35c8-155">-WebApp</span></span>
<span data-ttu-id="b35c8-156">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="b35c8-156">WebApp Object</span></span>

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

### <span data-ttu-id="b35c8-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="b35c8-158">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b35c8-158">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="b35c8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35c8-159">CommonParameters</span></span>
<span data-ttu-id="b35c8-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35c8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35c8-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b35c8-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35c8-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b35c8-162">INPUTS</span></span>

### <span data-ttu-id="b35c8-163">Elementem</span><span class="sxs-lookup"><span data-stu-id="b35c8-163">Int32</span></span>
<span data-ttu-id="b35c8-164">Parametr "NumberOfWorkers" akceptuje wartość typu "Int32" z procesu</span><span class="sxs-lookup"><span data-stu-id="b35c8-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="b35c8-165">Klienta</span><span class="sxs-lookup"><span data-stu-id="b35c8-165">Site</span></span>
<span data-ttu-id="b35c8-166">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="b35c8-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b35c8-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b35c8-167">OUTPUTS</span></span>

## <span data-ttu-id="b35c8-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b35c8-168">NOTES</span></span>

## <span data-ttu-id="b35c8-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b35c8-169">RELATED LINKS</span></span>

[<span data-ttu-id="b35c8-170">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b35c8-171">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b35c8-172">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b35c8-173">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b35c8-174">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b35c8-175">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b35c8-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
