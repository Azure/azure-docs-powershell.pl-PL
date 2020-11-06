---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528173"
---
# <span data-ttu-id="1d787-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="1d787-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d787-102">SYNOPSIS</span></span>
<span data-ttu-id="1d787-103">Modyfikuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1d787-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d787-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d787-104">SYNTAX</span></span>

### <span data-ttu-id="1d787-105">S1</span><span class="sxs-lookup"><span data-stu-id="1d787-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d787-106">S2</span><span class="sxs-lookup"><span data-stu-id="1d787-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d787-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d787-107">DESCRIPTION</span></span>
<span data-ttu-id="1d787-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1d787-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="1d787-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d787-109">EXAMPLES</span></span>

### <span data-ttu-id="1d787-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d787-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="1d787-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla aplikacji sieci Web ContosoWebApp skojarzonych z domyślnym grupą zasobów — sieć Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="1d787-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="1d787-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d787-112">PARAMETERS</span></span>

### <span data-ttu-id="1d787-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1d787-113">-AppServicePlan</span></span>
<span data-ttu-id="1d787-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="1d787-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="1d787-115">-AppSettings</span></span>
<span data-ttu-id="1d787-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="1d787-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="1d787-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="1d787-118">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="1d787-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="1d787-119">-ConnectionStrings</span></span>
<span data-ttu-id="1d787-120">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="1d787-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="1d787-121">-DefaultDocuments</span></span>
<span data-ttu-id="1d787-122">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="1d787-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="1d787-124">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="1d787-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="1d787-125">-HandlerMappings</span></span>
<span data-ttu-id="1d787-126">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="1d787-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="1d787-127">-Nazwa_hostas</span><span class="sxs-lookup"><span data-stu-id="1d787-127">-HostNames</span></span>
<span data-ttu-id="1d787-128">Tablica ciągów nazw aplikacji</span><span class="sxs-lookup"><span data-stu-id="1d787-128">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="1d787-130">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="1d787-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="1d787-132">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="1d787-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d787-133">-Name</span></span>
<span data-ttu-id="1d787-134">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1d787-134">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="1d787-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="1d787-136">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="1d787-136">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="1d787-137">-NumberOfWorkers</span></span>
<span data-ttu-id="1d787-138">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="1d787-138">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="1d787-139">-PhpVersion</span></span>
<span data-ttu-id="1d787-140">Wersja php</span><span class="sxs-lookup"><span data-stu-id="1d787-140">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="1d787-142">Włączone śledzenie żądań</span><span class="sxs-lookup"><span data-stu-id="1d787-142">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d787-143">-ResourceGroupName</span></span>
<span data-ttu-id="1d787-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d787-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="1d787-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="1d787-146">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="1d787-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-147">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1d787-147">-WebApp</span></span>
<span data-ttu-id="1d787-148">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="1d787-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="1d787-150">Wartość logiczna WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="1d787-150">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d787-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d787-151">-DefaultProfile</span></span>
<span data-ttu-id="1d787-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d787-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d787-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d787-153">CommonParameters</span></span>
<span data-ttu-id="1d787-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d787-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d787-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d787-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d787-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d787-156">INPUTS</span></span>

### <span data-ttu-id="1d787-157">Elementem</span><span class="sxs-lookup"><span data-stu-id="1d787-157">Int32</span></span>
<span data-ttu-id="1d787-158">Parametr "NumberOfWorkers" akceptuje wartość typu "Int32" z procesu</span><span class="sxs-lookup"><span data-stu-id="1d787-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="1d787-159">Klienta</span><span class="sxs-lookup"><span data-stu-id="1d787-159">Site</span></span>
<span data-ttu-id="1d787-160">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="1d787-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1d787-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d787-161">OUTPUTS</span></span>

## <span data-ttu-id="1d787-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d787-162">NOTES</span></span>

## <span data-ttu-id="1d787-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d787-163">RELATED LINKS</span></span>

[<span data-ttu-id="1d787-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1d787-165">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1d787-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1d787-167">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1d787-168">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1d787-169">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1d787-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
