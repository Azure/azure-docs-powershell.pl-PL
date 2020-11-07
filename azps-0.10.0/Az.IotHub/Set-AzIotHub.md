---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: d6aa49cce1a97d0177c66dd735180df2fa46c97d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891341"
---
# <span data-ttu-id="5cbb4-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="5cbb4-101">Set-AzIotHub</span></span>

## <span data-ttu-id="5cbb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cbb4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbb4-103">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="5cbb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cbb4-104">SYNTAX</span></span>

### <span data-ttu-id="5cbb4-105">UpdateSku (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5cbb4-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cbb4-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="5cbb4-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbb4-112">Opis</span><span class="sxs-lookup"><span data-stu-id="5cbb4-112">DESCRIPTION</span></span>
<span data-ttu-id="5cbb4-113">Aktualizuje właściwości IotHub.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="5cbb4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cbb4-114">EXAMPLES</span></span>

### <span data-ttu-id="5cbb4-115">Przykład 1 Aktualizowanie wersji SKU</span><span class="sxs-lookup"><span data-stu-id="5cbb4-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="5cbb4-116">Zaktualizuj jednostkę SKU do poziomu S1 oraz jednostki do 5 dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="5cbb4-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="5cbb4-117">Przykład 2 aktualizowanie właściwości centrum eventhub</span><span class="sxs-lookup"><span data-stu-id="5cbb4-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="5cbb4-118">Aktualizowanie czasu przechowywania danych telemetrycznych w dniach do 4 dla IotHub o nazwie "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5cbb4-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5cbb4-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cbb4-119">PARAMETERS</span></span>

### <span data-ttu-id="5cbb4-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="5cbb4-120">-CloudToDevice</span></span>
<span data-ttu-id="5cbb4-121">Właściwości kolejki poleceń chmury na urządzenie.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-121">The properties for the cloud to device command queue.</span></span> 

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

### <span data-ttu-id="5cbb4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbb4-122">-DefaultProfile</span></span>
<span data-ttu-id="5cbb4-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5cbb4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cbb4-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="5cbb4-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="5cbb4-125">Flaga określająca, czy w przypadku przekazywania pliku mają być włączone powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

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

### <span data-ttu-id="5cbb4-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="5cbb4-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="5cbb4-127">Czas przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-127">Retention time in days.</span></span> 

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

### <span data-ttu-id="5cbb4-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="5cbb4-128">-FallbackRoute</span></span>
<span data-ttu-id="5cbb4-129">Alternatywna trasa routingu</span><span class="sxs-lookup"><span data-stu-id="5cbb4-129">Fallback Route for Routing</span></span>

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

### <span data-ttu-id="5cbb4-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="5cbb4-130">-FileUploadContainerName</span></span>
<span data-ttu-id="5cbb4-131">Nazwa kontenera, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-131">The name of the container to upload the files to.</span></span>

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

### <span data-ttu-id="5cbb4-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="5cbb4-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="5cbb4-133">Maksymalna liczba dostaw dla powiadomień o przekazywaniu plików.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-133">The maximum delivery count for file upload notifications.</span></span>  

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

### <span data-ttu-id="5cbb4-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="5cbb4-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="5cbb4-135">Wartość czasu wygaśnięcia dla wiadomości w kolejce powiadomień przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-135">Time to live value for the messages in the file upload notification queue.</span></span> 

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

### <span data-ttu-id="5cbb4-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="5cbb4-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="5cbb4-137">Czas wygaśnięcia dla identyfikatora URI SAS wygenerowanego dla przekazywania plików.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

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

### <span data-ttu-id="5cbb4-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="5cbb4-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="5cbb4-139">Parametry połączenia z magazynem, do którego mają być przekazywane pliki.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-139">The storage connection string to upload the files to.</span></span> 

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

### <span data-ttu-id="5cbb4-140">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5cbb4-140">-Name</span></span>
<span data-ttu-id="5cbb4-141">Nazwa IotHub</span><span class="sxs-lookup"><span data-stu-id="5cbb4-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="5cbb4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cbb4-142">-ResourceGroupName</span></span>
<span data-ttu-id="5cbb4-143">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5cbb4-143">Resource Group Name</span></span>

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

### <span data-ttu-id="5cbb4-144">-Routes</span><span class="sxs-lookup"><span data-stu-id="5cbb4-144">-Routes</span></span>
<span data-ttu-id="5cbb4-145">Trasy do dodania do routingu</span><span class="sxs-lookup"><span data-stu-id="5cbb4-145">Routes to be added for Routing</span></span>

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

### <span data-ttu-id="5cbb4-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="5cbb4-146">-RoutingProperties</span></span>
<span data-ttu-id="5cbb4-147">Właściwości routingu do routowania wiadomości do zewnętrznych punktów końcowych</span><span class="sxs-lookup"><span data-stu-id="5cbb4-147">The Routing properties for routing messages to external endpoints</span></span> 

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

### <span data-ttu-id="5cbb4-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5cbb4-148">-SkuName</span></span>
<span data-ttu-id="5cbb4-149">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-149">Name of the Sku.</span></span>

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

### <span data-ttu-id="5cbb4-150">-Jednostki</span><span class="sxs-lookup"><span data-stu-id="5cbb4-150">-Units</span></span>
<span data-ttu-id="5cbb4-151">Liczba jednostek</span><span class="sxs-lookup"><span data-stu-id="5cbb4-151">Number of Units</span></span>

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

### <span data-ttu-id="5cbb4-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5cbb4-152">-Confirm</span></span>
<span data-ttu-id="5cbb4-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbb4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cbb4-154">-WhatIf</span></span>
<span data-ttu-id="5cbb4-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cbb4-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbb4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbb4-157">CommonParameters</span></span>
<span data-ttu-id="5cbb4-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbb4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbb4-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cbb4-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbb4-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cbb4-160">INPUTS</span></span>

### <span data-ttu-id="5cbb4-161">System. String</span><span class="sxs-lookup"><span data-stu-id="5cbb4-161">System.String</span></span>

## <span data-ttu-id="5cbb4-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cbb4-162">OUTPUTS</span></span>

### <span data-ttu-id="5cbb4-163">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5cbb4-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="5cbb4-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cbb4-164">NOTES</span></span>

## <span data-ttu-id="5cbb4-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cbb4-165">RELATED LINKS</span></span>
