---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055170"
---
# <span data-ttu-id="67d04-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67d04-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="67d04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67d04-102">SYNOPSIS</span></span>
<span data-ttu-id="67d04-103">Tworzy nowe konto magazynu w ramach subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="67d04-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="67d04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67d04-104">SYNTAX</span></span>

### <span data-ttu-id="67d04-105">ParameterSetAffinityGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="67d04-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="67d04-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="67d04-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="67d04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="67d04-107">DESCRIPTION</span></span>
<span data-ttu-id="67d04-108">Polecenie cmdlet **New-AzureStorageAccount** umożliwia utworzenie konta zapewniającego dostęp do usług Azure Storage Services.</span><span class="sxs-lookup"><span data-stu-id="67d04-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="67d04-109">Konto magazynu to globalny unikatowy zasób w systemie magazynowania.</span><span class="sxs-lookup"><span data-stu-id="67d04-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="67d04-110">Konto jest nadrzędną przestrzenią nazw dla obiektu BLOB, kolejki i usług tabel.</span><span class="sxs-lookup"><span data-stu-id="67d04-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="67d04-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67d04-111">EXAMPLES</span></span>

### <span data-ttu-id="67d04-112">Przykład 1. Tworzenie konta magazynu dla określonej grupy koligacji</span><span class="sxs-lookup"><span data-stu-id="67d04-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="67d04-113">To polecenie tworzy konto magazynu dla określonej grupy koligacji.</span><span class="sxs-lookup"><span data-stu-id="67d04-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="67d04-114">Przykład 2: Tworzenie konta magazynu w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="67d04-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="67d04-115">To polecenie tworzy konto magazynu w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="67d04-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="67d04-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67d04-116">PARAMETERS</span></span>

### <span data-ttu-id="67d04-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="67d04-117">-AffinityGroup</span></span>
<span data-ttu-id="67d04-118">Określa nazwę istniejącej grupy koligacji w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="67d04-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="67d04-119">Możesz określić parametr *Lokalizacja* lub *AffinityGroup* , ale nie oba.</span><span class="sxs-lookup"><span data-stu-id="67d04-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="67d04-120">-Description</span></span>
<span data-ttu-id="67d04-121">Określa opis konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="67d04-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="67d04-122">Długość opisu może wynosić do 1024 znaków.</span><span class="sxs-lookup"><span data-stu-id="67d04-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67d04-123">-InformationAction</span></span>
<span data-ttu-id="67d04-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="67d04-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67d04-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="67d04-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67d04-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="67d04-126">Continue</span></span>
- <span data-ttu-id="67d04-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="67d04-127">Ignore</span></span>
- <span data-ttu-id="67d04-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="67d04-128">Inquire</span></span>
- <span data-ttu-id="67d04-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67d04-129">SilentlyContinue</span></span>
- <span data-ttu-id="67d04-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="67d04-130">Stop</span></span>
- <span data-ttu-id="67d04-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="67d04-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67d04-132">-InformationVariable</span></span>
<span data-ttu-id="67d04-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="67d04-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-134">-Label</span><span class="sxs-lookup"><span data-stu-id="67d04-134">-Label</span></span>
<span data-ttu-id="67d04-135">Określa etykietę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="67d04-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="67d04-136">Etykieta może mieć długość do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="67d04-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="67d04-137">-Location</span></span>
<span data-ttu-id="67d04-138">Określa lokalizację usługi Azure Data Center, w której jest tworzone konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="67d04-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="67d04-139">Możesz dodać parametr *lokalizacji* lub *AffinityGroup* , ale nie oba.</span><span class="sxs-lookup"><span data-stu-id="67d04-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="67d04-140">-Profile</span></span>
<span data-ttu-id="67d04-141">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d04-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67d04-142">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="67d04-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="67d04-143">-StorageAccountName</span></span>
<span data-ttu-id="67d04-144">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="67d04-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="67d04-145">Nazwa konta magazynu musi być unikatowa na platformie Azure i musi mieć długość od 3 do 24 znaków i zawierać tylko małe litery i cyfry.</span><span class="sxs-lookup"><span data-stu-id="67d04-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-146">-Type</span><span class="sxs-lookup"><span data-stu-id="67d04-146">-Type</span></span>
<span data-ttu-id="67d04-147">Określa typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="67d04-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="67d04-148">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="67d04-148">Valid values are:</span></span>

- <span data-ttu-id="67d04-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="67d04-149">Standard_LRS</span></span>
- <span data-ttu-id="67d04-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="67d04-150">Standard_ZRS</span></span>
- <span data-ttu-id="67d04-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="67d04-151">Standard_GRS</span></span>
- <span data-ttu-id="67d04-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="67d04-152">Standard_RAGRS</span></span>
- <span data-ttu-id="67d04-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="67d04-153">Premium_LRS</span></span>

<span data-ttu-id="67d04-154">Jeśli ten parametr nie jest określony, wartością domyślną jest Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="67d04-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="67d04-155">Konta Standard_ZRS lub Premium_LRS nie mogą być zmieniane na inne typy kont i odwrotnie.</span><span class="sxs-lookup"><span data-stu-id="67d04-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d04-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d04-156">CommonParameters</span></span>
<span data-ttu-id="67d04-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d04-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d04-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d04-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d04-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67d04-159">INPUTS</span></span>

## <span data-ttu-id="67d04-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67d04-160">OUTPUTS</span></span>

## <span data-ttu-id="67d04-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67d04-161">NOTES</span></span>

## <span data-ttu-id="67d04-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67d04-162">RELATED LINKS</span></span>

[<span data-ttu-id="67d04-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67d04-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="67d04-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="67d04-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


