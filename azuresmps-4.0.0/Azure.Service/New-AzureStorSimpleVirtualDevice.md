---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054477"
---
# <span data-ttu-id="17b2a-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="17b2a-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="17b2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="17b2a-103">Umożliwia utworzenie wirtualnego urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="17b2a-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="17b2a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17b2a-104">SYNTAX</span></span>

### <span data-ttu-id="17b2a-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17b2a-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="17b2a-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17b2a-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17b2a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="17b2a-107">DESCRIPTION</span></span>
<span data-ttu-id="17b2a-108">Polecenie cmdlet **New-AzureStorSimpleVirtualDevice** umożliwia utworzenie wirtualnego urządzenia StorSimple.</span><span class="sxs-lookup"><span data-stu-id="17b2a-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="17b2a-109">Określ nazwę urządzenia dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="17b2a-109">Specify a device name for the device.</span></span>
<span data-ttu-id="17b2a-110">Określanie sieci wirtualnej i szczegółów podsieci dla sieci wirtualnej w tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="17b2a-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="17b2a-111">Lokalizację geograficzną należy dopasować do geograficznej, w której jest tworzony zasób StorSimple.</span><span class="sxs-lookup"><span data-stu-id="17b2a-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="17b2a-112">Aby użyć istniejącego konta magazynu dla tego urządzenia wirtualnego, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="17b2a-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="17b2a-113">Aby utworzyć nowe konto magazynu dla tego urządzenia wirtualnego, określ zarówno parametry *StorageAccountName* , jak i *CreateNewStorageAccount* .</span><span class="sxs-lookup"><span data-stu-id="17b2a-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="17b2a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17b2a-114">EXAMPLES</span></span>

### <span data-ttu-id="17b2a-115">Przykład 1. Tworzenie urządzenia wirtualnego z nowym kontem i istniejącą siecią</span><span class="sxs-lookup"><span data-stu-id="17b2a-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="17b2a-116">To polecenie tworzy urządzenie wirtualne korzystające z nowego konta magazynu i istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17b2a-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="17b2a-117">Przykład 2: Tworzenie urządzenia wirtualnego z istniejącym kontem i siecią wirtualną</span><span class="sxs-lookup"><span data-stu-id="17b2a-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="17b2a-118">To polecenie tworzy urządzenie wirtualne korzystające z istniejącego konta magazynu i istniejącej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17b2a-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="17b2a-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17b2a-119">PARAMETERS</span></span>

### <span data-ttu-id="17b2a-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="17b2a-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="17b2a-121">Wskazuje, że to polecenie cmdlet tworzy nowe konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="17b2a-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2a-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="17b2a-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="17b2a-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="17b2a-123">-Profile</span></span>
<span data-ttu-id="17b2a-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17b2a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17b2a-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="17b2a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17b2a-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="17b2a-126">-StorageAccountName</span></span>
<span data-ttu-id="17b2a-127">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="17b2a-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2a-128">-SubNetname</span><span class="sxs-lookup"><span data-stu-id="17b2a-128">-SubNetName</span></span>
<span data-ttu-id="17b2a-129">Określa nazwę podsieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17b2a-129">Specifies the name of a virtual subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2a-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="17b2a-130">-VirtualDeviceName</span></span>
<span data-ttu-id="17b2a-131">Określa nazwę urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="17b2a-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2a-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="17b2a-132">-VirtualNetworkName</span></span>
<span data-ttu-id="17b2a-133">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="17b2a-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b2a-134">CommonParameters</span></span>
<span data-ttu-id="17b2a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b2a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b2a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b2a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17b2a-137">INPUTS</span></span>

## <span data-ttu-id="17b2a-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17b2a-138">OUTPUTS</span></span>

### <span data-ttu-id="17b2a-139">Ciąg</span><span class="sxs-lookup"><span data-stu-id="17b2a-139">String</span></span>
<span data-ttu-id="17b2a-140">To polecenie cmdlet zwraca identyfikator zadania, które powoduje utworzenie urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="17b2a-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="17b2a-141">Możesz użyć tego identyfikatora, aby śledzić postęp za pomocą polecenia cmdlet Get-AzureStorSimpleJob.</span><span class="sxs-lookup"><span data-stu-id="17b2a-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="17b2a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17b2a-142">NOTES</span></span>

## <span data-ttu-id="17b2a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17b2a-143">RELATED LINKS</span></span>

[<span data-ttu-id="17b2a-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="17b2a-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="17b2a-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="17b2a-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


