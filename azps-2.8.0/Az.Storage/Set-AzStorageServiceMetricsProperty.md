---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 21bac0db2ca35a94edc80fd8f17ad85361883007
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704803"
---
# <span data-ttu-id="d8683-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d8683-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="d8683-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8683-102">SYNOPSIS</span></span>
<span data-ttu-id="d8683-103">Modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d8683-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="d8683-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8683-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8683-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8683-105">DESCRIPTION</span></span>
<span data-ttu-id="d8683-106">Polecenie cmdlet **Set-AzStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d8683-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="d8683-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8683-107">EXAMPLES</span></span>

### <span data-ttu-id="d8683-108">Przykład 1: modyfikowanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="d8683-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="d8683-109">To polecenie modyfikuje metryki w wersji 1,0 dla magazynu obiektów BLOB na poziom usług.</span><span class="sxs-lookup"><span data-stu-id="d8683-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="d8683-110">Metryki usługi Azure Storage są zachowywanie wpisów przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="d8683-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="d8683-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla właściwości zmodyfikowano metryki.</span><span class="sxs-lookup"><span data-stu-id="d8683-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="d8683-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8683-112">PARAMETERS</span></span>

### <span data-ttu-id="d8683-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d8683-113">-Context</span></span>
<span data-ttu-id="d8683-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d8683-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d8683-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d8683-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d8683-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8683-116">-DefaultProfile</span></span>
<span data-ttu-id="d8683-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8683-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8683-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="d8683-118">-MetricsLevel</span></span>
<span data-ttu-id="d8683-119">Określa poziom metryk używany dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d8683-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="d8683-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8683-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8683-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d8683-121">None</span></span>
- <span data-ttu-id="d8683-122">Służby</span><span class="sxs-lookup"><span data-stu-id="d8683-122">Service</span></span>
- <span data-ttu-id="d8683-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="d8683-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="d8683-124">-Metryki</span><span class="sxs-lookup"><span data-stu-id="d8683-124">-MetricsType</span></span>
<span data-ttu-id="d8683-125">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="d8683-125">Specifies a metrics type.</span></span>
<span data-ttu-id="d8683-126">To polecenie cmdlet ustawia typ metryki usługi Azure Storage na wartość określającą wartość tego parametru.</span><span class="sxs-lookup"><span data-stu-id="d8683-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="d8683-127">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="d8683-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="d8683-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8683-128">-PassThru</span></span>
<span data-ttu-id="d8683-129">Wskazuje, że te polecenia cmdlet zwracają zaktualizowane właściwości metryk.</span><span class="sxs-lookup"><span data-stu-id="d8683-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="d8683-130">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="d8683-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d8683-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="d8683-131">-RetentionDays</span></span>
<span data-ttu-id="d8683-132">Określa liczbę dni przechowywania informacji o metrykach w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="d8683-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="d8683-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d8683-133">-ServiceType</span></span>
<span data-ttu-id="d8683-134">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8683-134">Specifies the storage service type.</span></span>
<span data-ttu-id="d8683-135">To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d8683-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="d8683-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d8683-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8683-137">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="d8683-137">Blob</span></span> 
- <span data-ttu-id="d8683-138">Tworząc</span><span class="sxs-lookup"><span data-stu-id="d8683-138">Table</span></span>
- <span data-ttu-id="d8683-139">Wykonany</span><span class="sxs-lookup"><span data-stu-id="d8683-139">Queue</span></span>
- <span data-ttu-id="d8683-140">Plik wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="d8683-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="d8683-141">-Version</span><span class="sxs-lookup"><span data-stu-id="d8683-141">-Version</span></span>
<span data-ttu-id="d8683-142">Określa wersję metryk magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8683-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="d8683-143">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="d8683-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="d8683-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8683-144">CommonParameters</span></span>
<span data-ttu-id="d8683-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8683-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8683-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8683-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8683-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8683-147">INPUTS</span></span>

### <span data-ttu-id="d8683-148">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8683-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d8683-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8683-149">OUTPUTS</span></span>

### <span data-ttu-id="d8683-150">Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="d8683-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="d8683-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8683-151">NOTES</span></span>

## <span data-ttu-id="d8683-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8683-152">RELATED LINKS</span></span>

[<span data-ttu-id="d8683-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d8683-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="d8683-154">Nowe — AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8683-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

