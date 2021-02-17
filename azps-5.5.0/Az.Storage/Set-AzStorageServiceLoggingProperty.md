---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241794"
---
# <span data-ttu-id="6190f-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6190f-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="6190f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6190f-102">SYNOPSIS</span></span>
<span data-ttu-id="6190f-103">Modyfikuje rejestrowanie dla usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="6190f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6190f-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6190f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6190f-105">DESCRIPTION</span></span>
<span data-ttu-id="6190f-106">Polecenie **cmdlet Set-AzStorageServiceLoggingProperty** modyfikuje rejestrowanie dla usług magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="6190f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6190f-107">EXAMPLES</span></span>

### <span data-ttu-id="6190f-108">Przykład 1. Modyfikowanie właściwości rejestrowania dla usługi obiektów blob</span><span class="sxs-lookup"><span data-stu-id="6190f-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="6190f-109">To polecenie modyfikuje rejestrowanie dla magazynu obiektów blob w wersji 1.0 w celu dołączyć operacje odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="6190f-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="6190f-110">Rejestrowanie usługi magazynu platformy Azure zachowuje wpisy przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="6190f-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="6190f-111">To polecenie określa parametr *PassThru,* dlatego wyświetla zmodyfikowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="6190f-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="6190f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6190f-112">PARAMETERS</span></span>

### <span data-ttu-id="6190f-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="6190f-113">-Context</span></span>
<span data-ttu-id="6190f-114">Określa kontekst magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6190f-115">Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6190f-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6190f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6190f-116">-DefaultProfile</span></span>
<span data-ttu-id="6190f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6190f-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="6190f-118">-LoggingOperations</span></span>
<span data-ttu-id="6190f-119">Określa tablicę operacji usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="6190f-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="6190f-120">Usługi magazynu platformy Azure rejestruje operacje, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6190f-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="6190f-121">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6190f-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6190f-122">Brak</span><span class="sxs-lookup"><span data-stu-id="6190f-122">None</span></span>
- <span data-ttu-id="6190f-123">Czytanie</span><span class="sxs-lookup"><span data-stu-id="6190f-123">Read</span></span>
- <span data-ttu-id="6190f-124">Pisanie</span><span class="sxs-lookup"><span data-stu-id="6190f-124">Write</span></span>
- <span data-ttu-id="6190f-125">Usuń</span><span class="sxs-lookup"><span data-stu-id="6190f-125">Delete</span></span>
- <span data-ttu-id="6190f-126">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="6190f-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6190f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6190f-127">-PassThru</span></span>
<span data-ttu-id="6190f-128">Wskazuje, że to polecenie cmdlet zwraca zaktualizowane właściwości rejestrowania.</span><span class="sxs-lookup"><span data-stu-id="6190f-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="6190f-129">Jeśli nie określisz tego parametru, to polecenie cmdlet nie zwróci wartości.</span><span class="sxs-lookup"><span data-stu-id="6190f-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6190f-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="6190f-130">-RetentionDays</span></span>
<span data-ttu-id="6190f-131">Określa liczbę dni przechowywania zarejestrowanych informacji przez usługę magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="6190f-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6190f-132">-ServiceType</span></span>
<span data-ttu-id="6190f-133">Określa typ usługi magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6190f-133">Specifies the storage service type.</span></span>
<span data-ttu-id="6190f-134">To polecenie cmdlet modyfikuje właściwości rejestrowania dla typu usługi, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="6190f-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="6190f-135">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6190f-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6190f-136">Obiekt blob</span><span class="sxs-lookup"><span data-stu-id="6190f-136">Blob</span></span> 
- <span data-ttu-id="6190f-137">Tabela</span><span class="sxs-lookup"><span data-stu-id="6190f-137">Table</span></span>
- <span data-ttu-id="6190f-138">Kolejka</span><span class="sxs-lookup"><span data-stu-id="6190f-138">Queue</span></span>
- <span data-ttu-id="6190f-139">Plik Wartość pliku nie jest obecnie obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="6190f-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6190f-140">— Wersja</span><span class="sxs-lookup"><span data-stu-id="6190f-140">-Version</span></span>
<span data-ttu-id="6190f-141">Określa wersję rejestrowania usługi magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6190f-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="6190f-142">Wartość domyślna to 1,0.</span><span class="sxs-lookup"><span data-stu-id="6190f-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="6190f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6190f-143">CommonParameters</span></span>
<span data-ttu-id="6190f-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6190f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6190f-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6190f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6190f-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6190f-146">INPUTS</span></span>

### <span data-ttu-id="6190f-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6190f-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6190f-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6190f-148">OUTPUTS</span></span>

### <span data-ttu-id="6190f-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="6190f-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="6190f-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6190f-150">NOTES</span></span>

## <span data-ttu-id="6190f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6190f-151">RELATED LINKS</span></span>

[<span data-ttu-id="6190f-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6190f-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="6190f-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6190f-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


