---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: aad54e42d628239f087e376eabe6b9950c07b6f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553280"
---
# <span data-ttu-id="300e4-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="300e4-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="300e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="300e4-102">SYNOPSIS</span></span>
<span data-ttu-id="300e4-103">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="300e4-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="300e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="300e4-104">SYNTAX</span></span>

### <span data-ttu-id="300e4-105">UpdateSku (domyślny)</span><span class="sxs-lookup"><span data-stu-id="300e4-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="300e4-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="300e4-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="300e4-113">Opis</span><span class="sxs-lookup"><span data-stu-id="300e4-113">DESCRIPTION</span></span>
<span data-ttu-id="300e4-114">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="300e4-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="300e4-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="300e4-115">EXAMPLES</span></span>

### <span data-ttu-id="300e4-116">Przykład 1 Aktualizowanie wersji SKU</span><span class="sxs-lookup"><span data-stu-id="300e4-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="300e4-117">Zaktualizuj jednostkę SKU do poziomu S1 oraz jednostki do 5 dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="300e4-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="300e4-118">Przykład 2 aktualizowanie właściwości centrum eventhub</span><span class="sxs-lookup"><span data-stu-id="300e4-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="300e4-119">Aktualizowanie czasu przechowywania w dniach do 4 zarówno dla zdarzeń telemetrii, jak i operationsmonitoringevents dla IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="300e4-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="300e4-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="300e4-120">PARAMETERS</span></span>

### <span data-ttu-id="300e4-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="300e4-121">-CloudToDevice</span></span>
<span data-ttu-id="300e4-122">Właściwości kolejki poleceń chmury na urządzenie.</span><span class="sxs-lookup"><span data-stu-id="300e4-122">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-123">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="300e4-123">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="300e4-124">Flaga określająca, czy w przypadku przekazywania pliku mają być włączone powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="300e4-124">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-125">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="300e4-125">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="300e4-126">Czas przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="300e4-126">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-127">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="300e4-127">-FallbackRoute</span></span>
<span data-ttu-id="300e4-128">Alternatywna trasa routingu</span><span class="sxs-lookup"><span data-stu-id="300e4-128">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-129">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="300e4-129">-FileUploadContainerName</span></span>
<span data-ttu-id="300e4-130">Nazwa kontenera, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="300e4-130">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-131">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="300e4-131">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="300e4-132">Maksymalna liczba dostaw dla powiadomień o przekazywaniu plików.</span><span class="sxs-lookup"><span data-stu-id="300e4-132">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-133">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="300e4-133">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="300e4-134">Wartość czasu wygaśnięcia dla wiadomości w kolejce powiadomień przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="300e4-134">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-135">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="300e4-135">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="300e4-136">Czas wygaśnięcia dla identyfikatora URI SAS wygenerowanego dla przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="300e4-136">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-137">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="300e4-137">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="300e4-138">Parametry połączenia z magazynem, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="300e4-138">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="300e4-139">-Name</span></span>
<span data-ttu-id="300e4-140">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="300e4-140">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-141">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-141">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="300e4-142">Właściwości związane z monitorowaniem operacji.</span><span class="sxs-lookup"><span data-stu-id="300e4-142">The properties related to operations monitoring.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties
Parameter Sets: UpdateOperationsMonitoringProperties
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="300e4-143">-ResourceGroupName</span></span>
<span data-ttu-id="300e4-144">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="300e4-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-145">-Routes</span><span class="sxs-lookup"><span data-stu-id="300e4-145">-Routes</span></span>
<span data-ttu-id="300e4-146">Trasy do dodania do routingu</span><span class="sxs-lookup"><span data-stu-id="300e4-146">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-147">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-147">-RoutingProperties</span></span>
<span data-ttu-id="300e4-148">Właściwości routingu do routowania wiadomości do zewnętrznych punktów końcowych</span><span class="sxs-lookup"><span data-stu-id="300e4-148">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-149">-SkuName</span><span class="sxs-lookup"><span data-stu-id="300e4-149">-SkuName</span></span>
<span data-ttu-id="300e4-150">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="300e4-150">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-151">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="300e4-151">-Units</span></span>
<span data-ttu-id="300e4-152">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="300e4-152">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="300e4-153">-Confirm</span></span>
<span data-ttu-id="300e4-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="300e4-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="300e4-155">-WhatIf</span></span>
<span data-ttu-id="300e4-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="300e4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="300e4-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="300e4-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300e4-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300e4-158">-DefaultProfile</span></span>
<span data-ttu-id="300e4-159">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="300e4-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="300e4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300e4-160">CommonParameters</span></span>
<span data-ttu-id="300e4-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300e4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300e4-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300e4-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300e4-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="300e4-163">INPUTS</span></span>

### <span data-ttu-id="300e4-164">System. String</span><span class="sxs-lookup"><span data-stu-id="300e4-164">System.String</span></span>
<span data-ttu-id="300e4-165">Microsoft. Azure. Commands. Management. IotHub. models. PSCloudToDeviceProperties Microsoft. Azure. Commands. Management. IotHub. MODELES. PSOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="300e4-165">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties Microsoft.Azure.Commands.Management.IotHub.Models.PSOperationsMonitoringProperties</span></span>

## <span data-ttu-id="300e4-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="300e4-166">OUTPUTS</span></span>

### <span data-ttu-id="300e4-167">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="300e4-167">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="300e4-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="300e4-168">NOTES</span></span>

## <span data-ttu-id="300e4-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="300e4-169">RELATED LINKS</span></span>
