---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524125"
---
# <span data-ttu-id="9739e-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9739e-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="9739e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9739e-102">SYNOPSIS</span></span>
<span data-ttu-id="9739e-103">Modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9739e-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9739e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9739e-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9739e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9739e-105">DESCRIPTION</span></span>
<span data-ttu-id="9739e-106">Polecenie cmdlet **Set-AzureStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9739e-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="9739e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9739e-107">EXAMPLES</span></span>

### <span data-ttu-id="9739e-108">Przykład 1: modyfikowanie właściwości metryk dla usługi BLOB</span><span class="sxs-lookup"><span data-stu-id="9739e-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="9739e-109">To polecenie modyfikuje metryki w wersji 1,0 dla magazynu obiektów BLOB na poziom usług.</span><span class="sxs-lookup"><span data-stu-id="9739e-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="9739e-110">Metryki usługi Azure Storage są zachowywanie wpisów przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="9739e-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="9739e-111">Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla właściwości zmodyfikowano metryki.</span><span class="sxs-lookup"><span data-stu-id="9739e-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="9739e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9739e-112">PARAMETERS</span></span>

### <span data-ttu-id="9739e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9739e-113">-Context</span></span>
<span data-ttu-id="9739e-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9739e-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9739e-115">Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9739e-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="9739e-116">-MetricsLevel</span></span>
<span data-ttu-id="9739e-117">Określa poziom metryk używany dla usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9739e-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="9739e-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9739e-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9739e-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9739e-119">None</span></span>
- <span data-ttu-id="9739e-120">Służby</span><span class="sxs-lookup"><span data-stu-id="9739e-120">Service</span></span>
- <span data-ttu-id="9739e-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="9739e-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-122">-Metryki</span><span class="sxs-lookup"><span data-stu-id="9739e-122">-MetricsType</span></span>
<span data-ttu-id="9739e-123">Określa typ metryk.</span><span class="sxs-lookup"><span data-stu-id="9739e-123">Specifies a metrics type.</span></span>
<span data-ttu-id="9739e-124">Ten cmldet ustawia wartość typu metryki usługi Azure Storage na wartość określaną przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="9739e-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="9739e-125">Dopuszczalne wartości tego parametru to: godzina i minuta.</span><span class="sxs-lookup"><span data-stu-id="9739e-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9739e-126">-PassThru</span></span>
<span data-ttu-id="9739e-127">Wskazuje, że te polecenia cmdlet zwracają zaktualizowane właściwości metryk.</span><span class="sxs-lookup"><span data-stu-id="9739e-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="9739e-128">Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="9739e-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9739e-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="9739e-129">-RetentionDays</span></span>
<span data-ttu-id="9739e-130">Określa liczbę dni przechowywania informacji o metrykach w usłudze Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="9739e-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9739e-131">-ServiceType</span></span>
<span data-ttu-id="9739e-132">Określa typ usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="9739e-132">Specifies the storage service type.</span></span>
<span data-ttu-id="9739e-133">To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, którego ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="9739e-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="9739e-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9739e-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9739e-135">Obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="9739e-135">Blob</span></span> 
- <span data-ttu-id="9739e-136">Tworząc</span><span class="sxs-lookup"><span data-stu-id="9739e-136">Table</span></span>
- <span data-ttu-id="9739e-137">Wykonany</span><span class="sxs-lookup"><span data-stu-id="9739e-137">Queue</span></span>
- <span data-ttu-id="9739e-138">Plik</span><span class="sxs-lookup"><span data-stu-id="9739e-138">File</span></span>

<span data-ttu-id="9739e-139">Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="9739e-139">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-140">-Version</span><span class="sxs-lookup"><span data-stu-id="9739e-140">-Version</span></span>
<span data-ttu-id="9739e-141">Określa wersję metryk magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9739e-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="9739e-142">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="9739e-142">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9739e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9739e-143">CommonParameters</span></span>
<span data-ttu-id="9739e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9739e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9739e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9739e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9739e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9739e-146">INPUTS</span></span>

## <span data-ttu-id="9739e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9739e-147">OUTPUTS</span></span>

## <span data-ttu-id="9739e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9739e-148">NOTES</span></span>

## <span data-ttu-id="9739e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9739e-149">RELATED LINKS</span></span>

[<span data-ttu-id="9739e-150">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9739e-150">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="9739e-151">Nowe — AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9739e-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


