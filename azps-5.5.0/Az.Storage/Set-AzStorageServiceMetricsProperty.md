---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188850"
---
# <span data-ttu-id="afd37-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="afd37-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="afd37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd37-102">SYNOPSIS</span></span>
<span data-ttu-id="afd37-103">Modyfikuje właściwości metryk dla usługi magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afd37-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="afd37-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="afd37-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afd37-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="afd37-105">DESCRIPTION</span></span>
<span data-ttu-id="afd37-106">Polecenie cmdlet **Set-AzStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="afd37-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="afd37-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="afd37-107">EXAMPLES</span></span>

### <span data-ttu-id="afd37-108">Przykład 1. Modyfikowanie właściwości metryk dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="afd37-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="afd37-109">To polecenie modyfikuje metryki wersji 1.0 dla magazynu obiektów blob do poziomu usługi.</span><span class="sxs-lookup"><span data-stu-id="afd37-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="afd37-110">Metryki usługi magazynu Platformy Azure zachowują wpisy przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="afd37-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="afd37-111">To polecenie określa parametr *PassThru,* dlatego wyświetla właściwości zmodyfikowanych metryk.</span><span class="sxs-lookup"><span data-stu-id="afd37-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="afd37-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afd37-112">PARAMETERS</span></span>

### <span data-ttu-id="afd37-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="afd37-113">-Context</span></span>
<span data-ttu-id="afd37-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afd37-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="afd37-115">Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd37-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd37-116">-DefaultProfile</span></span>
<span data-ttu-id="afd37-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="afd37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="afd37-118">-MetricsLevel</span></span>
<span data-ttu-id="afd37-119">Określa poziom metryk używany przez usługę Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="afd37-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="afd37-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="afd37-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afd37-121">Brak</span><span class="sxs-lookup"><span data-stu-id="afd37-121">None</span></span>
- <span data-ttu-id="afd37-122">Usługa</span><span class="sxs-lookup"><span data-stu-id="afd37-122">Service</span></span>
- <span data-ttu-id="afd37-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="afd37-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="afd37-124">-MetricsType</span></span>
<span data-ttu-id="afd37-125">Określa typ metryki.</span><span class="sxs-lookup"><span data-stu-id="afd37-125">Specifies a metrics type.</span></span>
<span data-ttu-id="afd37-126">To polecenie cmdlet ustawia typ metryk usługi Azure Storage na wartość określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="afd37-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="afd37-127">Dopuszczalne wartości dla tego parametru to: Godzina i Minuta.</span><span class="sxs-lookup"><span data-stu-id="afd37-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd37-128">-PassThru</span></span>
<span data-ttu-id="afd37-129">Wskazuje, że te polecenia cmdlet zwraca właściwości zaktualizowanych metryk.</span><span class="sxs-lookup"><span data-stu-id="afd37-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="afd37-130">Jeśli nie określisz tego parametru, to polecenie cmdlet nie zwróci wartości.</span><span class="sxs-lookup"><span data-stu-id="afd37-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="afd37-131">-RetentionDays</span></span>
<span data-ttu-id="afd37-132">Określa liczbę dni, przez które usługa Magazynu Platformy Azure przechowuje informacje o metrykach.</span><span class="sxs-lookup"><span data-stu-id="afd37-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="afd37-133">-ServiceType</span></span>
<span data-ttu-id="afd37-134">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="afd37-134">Specifies the storage service type.</span></span>
<span data-ttu-id="afd37-135">To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="afd37-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="afd37-136">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="afd37-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="afd37-137">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="afd37-137">Blob</span></span> 
- <span data-ttu-id="afd37-138">Tabela</span><span class="sxs-lookup"><span data-stu-id="afd37-138">Table</span></span>
- <span data-ttu-id="afd37-139">Kolejka</span><span class="sxs-lookup"><span data-stu-id="afd37-139">Queue</span></span>
- <span data-ttu-id="afd37-140">Plik Wartość Pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="afd37-140">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-141">— Wersja</span><span class="sxs-lookup"><span data-stu-id="afd37-141">-Version</span></span>
<span data-ttu-id="afd37-142">Określa wersję metryk magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="afd37-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="afd37-143">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="afd37-143">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd37-144">CommonParameters</span></span>
<span data-ttu-id="afd37-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd37-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd37-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd37-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd37-147">INPUTS</span></span>

### <span data-ttu-id="afd37-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="afd37-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="afd37-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd37-149">OUTPUTS</span></span>

### <span data-ttu-id="afd37-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="afd37-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="afd37-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="afd37-151">NOTES</span></span>

## <span data-ttu-id="afd37-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afd37-152">RELATED LINKS</span></span>

[<span data-ttu-id="afd37-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="afd37-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="afd37-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="afd37-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


