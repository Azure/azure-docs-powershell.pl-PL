---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
ms.openlocfilehash: 1b32fbf01b22c365384190c6530a649a06664219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547743"
---
# <span data-ttu-id="04c0a-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="04c0a-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="04c0a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="04c0a-103">Modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04c0a-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c0a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04c0a-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c0a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="04c0a-106">Polecenie cmdlet **Set-AzureStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04c0a-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="04c0a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="04c0a-108">Przykład 1: modyfikowanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="04c0a-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="04c0a-109">To polecenie modyfikuje metryki w wersji 1,0 dla magazynu obiektów BLOB na poziom usług.</span><span class="sxs-lookup"><span data-stu-id="04c0a-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="04c0a-110">Metryki usługi Azure Storage są zachowywanie wpisów przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="04c0a-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="04c0a-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla właściwości zmodyfikowano metryki.</span><span class="sxs-lookup"><span data-stu-id="04c0a-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="04c0a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04c0a-112">PARAMETERS</span></span>

### <span data-ttu-id="04c0a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="04c0a-113">-Context</span></span>
<span data-ttu-id="04c0a-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04c0a-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04c0a-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="04c0a-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04c0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c0a-116">-DefaultProfile</span></span>
<span data-ttu-id="04c0a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04c0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c0a-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="04c0a-118">-MetricsLevel</span></span>
<span data-ttu-id="04c0a-119">Określa poziom metryk używany dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04c0a-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="04c0a-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04c0a-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04c0a-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="04c0a-121">None</span></span>
- <span data-ttu-id="04c0a-122">Służby</span><span class="sxs-lookup"><span data-stu-id="04c0a-122">Service</span></span>
- <span data-ttu-id="04c0a-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="04c0a-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04c0a-124">-Metryki</span><span class="sxs-lookup"><span data-stu-id="04c0a-124">-MetricsType</span></span>
<span data-ttu-id="04c0a-125">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="04c0a-125">Specifies a metrics type.</span></span>
<span data-ttu-id="04c0a-126">Ten cmldet ustawia wartość typu metryki usługi Azure Storage na wartość określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="04c0a-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="04c0a-127">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="04c0a-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="04c0a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04c0a-128">-PassThru</span></span>
<span data-ttu-id="04c0a-129">Wskazuje, że te polecenia cmdlet zwracają zaktualizowane właściwości metryk.</span><span class="sxs-lookup"><span data-stu-id="04c0a-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="04c0a-130">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="04c0a-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="04c0a-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="04c0a-131">-RetentionDays</span></span>
<span data-ttu-id="04c0a-132">Określa liczbę dni przechowywania informacji o metrykach w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="04c0a-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="04c0a-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="04c0a-133">-ServiceType</span></span>
<span data-ttu-id="04c0a-134">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="04c0a-134">Specifies the storage service type.</span></span>
<span data-ttu-id="04c0a-135">To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="04c0a-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="04c0a-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04c0a-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04c0a-137">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="04c0a-137">Blob</span></span> 
- <span data-ttu-id="04c0a-138">Tworząc</span><span class="sxs-lookup"><span data-stu-id="04c0a-138">Table</span></span>
- <span data-ttu-id="04c0a-139">Wykonany</span><span class="sxs-lookup"><span data-stu-id="04c0a-139">Queue</span></span>
- <span data-ttu-id="04c0a-140">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="04c0a-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="04c0a-141">-Version</span><span class="sxs-lookup"><span data-stu-id="04c0a-141">-Version</span></span>
<span data-ttu-id="04c0a-142">Określa wersję metryk magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="04c0a-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="04c0a-143">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="04c0a-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="04c0a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c0a-144">CommonParameters</span></span>
<span data-ttu-id="04c0a-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c0a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c0a-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c0a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c0a-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04c0a-147">INPUTS</span></span>

### <span data-ttu-id="04c0a-148">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04c0a-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04c0a-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04c0a-149">OUTPUTS</span></span>

### <span data-ttu-id="04c0a-150">Microsoft. platformy windowsazure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="04c0a-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="04c0a-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04c0a-151">NOTES</span></span>

## <span data-ttu-id="04c0a-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04c0a-152">RELATED LINKS</span></span>

[<span data-ttu-id="04c0a-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="04c0a-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="04c0a-154">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04c0a-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


