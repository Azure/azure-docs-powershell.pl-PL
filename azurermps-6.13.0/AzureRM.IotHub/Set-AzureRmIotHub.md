---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/set-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Set-AzureRmIotHub.md
ms.openlocfilehash: a6e4e9e87f43ee5796c47836c3fa29fcdbdb8f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718853"
---
# <span data-ttu-id="d643c-101">Set-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="d643c-101">Set-AzureRmIotHub</span></span>

## <span data-ttu-id="d643c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d643c-102">SYNOPSIS</span></span>
<span data-ttu-id="d643c-103">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="d643c-103">Updates the properties of an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d643c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d643c-104">SYNTAX</span></span>

### <span data-ttu-id="d643c-105">UpdateSku (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d643c-105">UpdateSku (Default)</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-107">UpdateFileUploadProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-109">UpdateOperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-109">UpdateOperationsMonitoringProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 -OperationsMonitoringProperties <PSOperationsMonitoringProperties> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-110">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-110">UpdateRoutingProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-111">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-111">UpdateRouteProperties</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d643c-112">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="d643c-112">UpdateFallbackRouteProperty</span></span>
```
Set-AzureRmIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d643c-113">Opis</span><span class="sxs-lookup"><span data-stu-id="d643c-113">DESCRIPTION</span></span>
<span data-ttu-id="d643c-114">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="d643c-114">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="d643c-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d643c-115">EXAMPLES</span></span>

### <span data-ttu-id="d643c-116">Przykład 1 Aktualizowanie wersji SKU</span><span class="sxs-lookup"><span data-stu-id="d643c-116">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="d643c-117">Zaktualizuj jednostkę SKU do poziomu S1 oraz jednostki do 5 dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d643c-117">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d643c-118">Przykład 2 aktualizowanie właściwości centrum eventhub</span><span class="sxs-lookup"><span data-stu-id="d643c-118">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="d643c-119">Aktualizowanie czasu przechowywania w dniach do 4 zarówno dla zdarzeń telemetrii, jak i operationsmonitoringevents dla IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d643c-119">Update the retention time in days to 4 for both the telemetry and operationsmonitoringevents events for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d643c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d643c-120">PARAMETERS</span></span>

### <span data-ttu-id="d643c-121">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="d643c-121">-CloudToDevice</span></span>
<span data-ttu-id="d643c-122">Właściwości kolejki poleceń chmury na urządzenie.</span><span class="sxs-lookup"><span data-stu-id="d643c-122">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="d643c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d643c-123">-DefaultProfile</span></span>
<span data-ttu-id="d643c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d643c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d643c-125">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="d643c-125">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="d643c-126">Flaga określająca, czy w przypadku przekazywania pliku mają być włączone powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="d643c-126">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="d643c-127">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="d643c-127">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="d643c-128">Czas przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="d643c-128">Retention time in days.</span></span> 

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

### <span data-ttu-id="d643c-129">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="d643c-129">-FallbackRoute</span></span>
<span data-ttu-id="d643c-130">Alternatywna trasa routingu</span><span class="sxs-lookup"><span data-stu-id="d643c-130">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="d643c-131">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="d643c-131">-FileUploadContainerName</span></span>
<span data-ttu-id="d643c-132">Nazwa kontenera, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="d643c-132">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="d643c-133">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d643c-133">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="d643c-134">Maksymalna liczba dostaw dla powiadomień o przekazywaniu plików.</span><span class="sxs-lookup"><span data-stu-id="d643c-134">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="d643c-135">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="d643c-135">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="d643c-136">Wartość czasu wygaśnięcia dla wiadomości w kolejce powiadomień przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="d643c-136">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="d643c-137">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="d643c-137">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="d643c-138">Czas wygaśnięcia dla identyfikatora URI SAS wygenerowanego dla przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="d643c-138">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="d643c-139">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="d643c-139">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="d643c-140">Parametry połączenia z magazynem, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="d643c-140">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="d643c-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d643c-141">-Name</span></span>
<span data-ttu-id="d643c-142">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="d643c-142">Name of the IotHub</span></span>

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

### <span data-ttu-id="d643c-143">-OperationsMonitoringProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-143">-OperationsMonitoringProperties</span></span>
<span data-ttu-id="d643c-144">Właściwości związane z monitorowaniem operacji.</span><span class="sxs-lookup"><span data-stu-id="d643c-144">The properties related to operations monitoring.</span></span> 

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

### <span data-ttu-id="d643c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d643c-145">-ResourceGroupName</span></span>
<span data-ttu-id="d643c-146">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d643c-146">Resource Group Name</span></span>

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

### <span data-ttu-id="d643c-147">-Routes</span><span class="sxs-lookup"><span data-stu-id="d643c-147">-Routes</span></span>
<span data-ttu-id="d643c-148">Trasy do dodania do routingu</span><span class="sxs-lookup"><span data-stu-id="d643c-148">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="d643c-149">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="d643c-149">-RoutingProperties</span></span>
<span data-ttu-id="d643c-150">Właściwości routingu do routowania wiadomości do zewnętrznych punktów końcowych</span><span class="sxs-lookup"><span data-stu-id="d643c-150">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="d643c-151">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d643c-151">-SkuName</span></span>
<span data-ttu-id="d643c-152">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="d643c-152">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d643c-153">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="d643c-153">-Units</span></span>
<span data-ttu-id="d643c-154">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="d643c-154">Number of Units</span></span>

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

### <span data-ttu-id="d643c-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d643c-155">-Confirm</span></span>
<span data-ttu-id="d643c-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d643c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d643c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d643c-157">-WhatIf</span></span>
<span data-ttu-id="d643c-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d643c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d643c-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d643c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d643c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d643c-160">CommonParameters</span></span>
<span data-ttu-id="d643c-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d643c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d643c-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d643c-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d643c-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d643c-163">INPUTS</span></span>

### <span data-ttu-id="d643c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d643c-164">System.String</span></span>

## <span data-ttu-id="d643c-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d643c-165">OUTPUTS</span></span>

### <span data-ttu-id="d643c-166">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d643c-166">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d643c-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d643c-167">NOTES</span></span>

## <span data-ttu-id="d643c-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d643c-168">RELATED LINKS</span></span>
