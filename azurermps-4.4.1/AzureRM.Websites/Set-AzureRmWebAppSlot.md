---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716518"
---
# <span data-ttu-id="05a51-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="05a51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05a51-102">SYNOPSIS</span></span>
<span data-ttu-id="05a51-103">Modyfikuje miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="05a51-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05a51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05a51-104">SYNTAX</span></span>

### <span data-ttu-id="05a51-105">S1</span><span class="sxs-lookup"><span data-stu-id="05a51-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05a51-106">S2</span><span class="sxs-lookup"><span data-stu-id="05a51-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05a51-107">Opis</span><span class="sxs-lookup"><span data-stu-id="05a51-107">DESCRIPTION</span></span>
<span data-ttu-id="05a51-108">Polecenie cmdlet **Set-AzureRmWebApp** ustawia miejsce w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="05a51-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="05a51-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05a51-109">EXAMPLES</span></span>

### <span data-ttu-id="05a51-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05a51-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="05a51-111">To polecenie ustawia HttpLoggingEnabled na wartość PRAWDA dla Slot001 gniazda odnoszącego się do aplikacji sieci Web ContosoWebApp skojarzonego z domyślnym grupą zasobów — sieć Web-zachód.</span><span class="sxs-lookup"><span data-stu-id="05a51-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="05a51-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05a51-112">PARAMETERS</span></span>

### <span data-ttu-id="05a51-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05a51-113">-AppServicePlan</span></span>
<span data-ttu-id="05a51-114">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="05a51-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="05a51-115">-AppSettings</span></span>
<span data-ttu-id="05a51-116">Obiekt HashTable ustawień aplikacji</span><span class="sxs-lookup"><span data-stu-id="05a51-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="05a51-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="05a51-118">Nazwa docelowego miejsca do automatycznego zamieniania</span><span class="sxs-lookup"><span data-stu-id="05a51-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="05a51-119">-ConnectionStrings</span></span>
<span data-ttu-id="05a51-120">Parametry połączenia HashTable</span><span class="sxs-lookup"><span data-stu-id="05a51-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="05a51-121">-DefaultDocuments</span></span>
<span data-ttu-id="05a51-122">Tablica ciągów w dokumentach domyślnych</span><span class="sxs-lookup"><span data-stu-id="05a51-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a51-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="05a51-124">Szczegółowy rejestrowanie błędów z włączoną wartością logiczną</span><span class="sxs-lookup"><span data-stu-id="05a51-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="05a51-125">-HandlerMappings</span></span>
<span data-ttu-id="05a51-126">Mapowania obsługi IList</span><span class="sxs-lookup"><span data-stu-id="05a51-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="05a51-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a51-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="05a51-128">Wartość logiczna HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a51-128">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="05a51-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="05a51-130">Nazwa zarządzanego trybu potokowego</span><span class="sxs-lookup"><span data-stu-id="05a51-130">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05a51-131">-Name</span></span>
<span data-ttu-id="05a51-132">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="05a51-132">WebApp Name</span></span>

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

### <span data-ttu-id="05a51-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="05a51-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="05a51-134">Wersja NET Framework</span><span class="sxs-lookup"><span data-stu-id="05a51-134">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="05a51-135">-NumberOfWorkers</span></span>
<span data-ttu-id="05a51-136">Liczba pracowników do przydzielenia</span><span class="sxs-lookup"><span data-stu-id="05a51-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="05a51-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="05a51-137">-PhpVersion</span></span>
<span data-ttu-id="05a51-138">Wersja php</span><span class="sxs-lookup"><span data-stu-id="05a51-138">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="05a51-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="05a51-140">Wartość logiczna włączonego śledzenia żądań</span><span class="sxs-lookup"><span data-stu-id="05a51-140">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05a51-141">-ResourceGroupName</span></span>
<span data-ttu-id="05a51-142">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="05a51-142">Resource Group Name</span></span>

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

### <span data-ttu-id="05a51-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="05a51-143">-Slot</span></span>
<span data-ttu-id="05a51-144">Nazwa gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="05a51-144">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="05a51-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="05a51-146">Użyj 32-bitowej wartości logicznej procesu roboczego</span><span class="sxs-lookup"><span data-stu-id="05a51-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05a51-147">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="05a51-147">-WebApp</span></span>
<span data-ttu-id="05a51-148">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="05a51-148">WebApp Object</span></span>

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

### <span data-ttu-id="05a51-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="05a51-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="05a51-150">Wartość logiczna z włączonymi gniazdami sieci Web</span><span class="sxs-lookup"><span data-stu-id="05a51-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="05a51-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a51-151">-DefaultProfile</span></span>
<span data-ttu-id="05a51-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05a51-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a51-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a51-153">CommonParameters</span></span>
<span data-ttu-id="05a51-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a51-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a51-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a51-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a51-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05a51-156">INPUTS</span></span>

### <span data-ttu-id="05a51-157">Elementem</span><span class="sxs-lookup"><span data-stu-id="05a51-157">Int32</span></span>
<span data-ttu-id="05a51-158">Parametr "NumberOfWorkers" akceptuje wartość typu "Int32" z procesu</span><span class="sxs-lookup"><span data-stu-id="05a51-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="05a51-159">Klienta</span><span class="sxs-lookup"><span data-stu-id="05a51-159">Site</span></span>
<span data-ttu-id="05a51-160">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="05a51-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="05a51-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05a51-161">OUTPUTS</span></span>

## <span data-ttu-id="05a51-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05a51-162">NOTES</span></span>

## <span data-ttu-id="05a51-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05a51-163">RELATED LINKS</span></span>

[<span data-ttu-id="05a51-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-165">Nowe — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-166">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-167">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-168">Start — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-169">Zatrzymaj — AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05a51-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="05a51-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05a51-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
