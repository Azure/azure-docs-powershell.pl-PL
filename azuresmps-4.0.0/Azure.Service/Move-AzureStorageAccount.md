---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055205"
---
# <span data-ttu-id="6b965-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6b965-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="6b965-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b965-102">SYNOPSIS</span></span>
<span data-ttu-id="6b965-103">Migruje konto magazynu do stosu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b965-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="6b965-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b965-104">SYNTAX</span></span>

### <span data-ttu-id="6b965-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b965-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b965-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b965-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b965-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b965-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b965-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b965-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b965-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6b965-109">DESCRIPTION</span></span>
<span data-ttu-id="6b965-110">Polecenie cmdlet **Move-AzureStorageAccount** Migruje konto magazynu do grupy zasobów na stosie usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b965-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="6b965-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b965-111">EXAMPLES</span></span>

### <span data-ttu-id="6b965-112">Przykład 1: przygotowywanie migracji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6b965-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="6b965-113">To polecenie przygotowuje konto magazynu o nazwie ContosoStorageName do migracji na stos Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6b965-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="6b965-114">Przykład 2: Rozpoczynanie migracji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="6b965-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="6b965-115">To polecenie rozpoczyna migrację konta magazynu o nazwie ContosoStorageName na stos usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b965-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="6b965-116">Przykład 3: weryfikowanie migracji kont magazynu</span><span class="sxs-lookup"><span data-stu-id="6b965-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="6b965-117">To polecenie sprawdza poprawność migracji konta magazynu o nazwie ContosoStorageName na stos usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6b965-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="6b965-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b965-118">PARAMETERS</span></span>

### <span data-ttu-id="6b965-119">-Przerwij</span><span class="sxs-lookup"><span data-stu-id="6b965-119">-Abort</span></span>
<span data-ttu-id="6b965-120">Wskazuje, że to polecenie cmdlet anuluje migrację konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6b965-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b965-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="6b965-121">-Commit</span></span>
<span data-ttu-id="6b965-122">Wskazuje, że to polecenie cmdlet rozpoczyna migrację konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6b965-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b965-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b965-123">-InformationAction</span></span>
<span data-ttu-id="6b965-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="6b965-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b965-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="6b965-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b965-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="6b965-126">Continue</span></span>
- <span data-ttu-id="6b965-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="6b965-127">Ignore</span></span>
- <span data-ttu-id="6b965-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="6b965-128">Inquire</span></span>
- <span data-ttu-id="6b965-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b965-129">SilentlyContinue</span></span>
- <span data-ttu-id="6b965-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="6b965-130">Stop</span></span>
- <span data-ttu-id="6b965-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="6b965-131">Suspend</span></span>

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

### <span data-ttu-id="6b965-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b965-132">-InformationVariable</span></span>
<span data-ttu-id="6b965-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="6b965-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b965-134">-Przygotuj</span><span class="sxs-lookup"><span data-stu-id="6b965-134">-Prepare</span></span>
<span data-ttu-id="6b965-135">Wskazuje, że to polecenie cmdlet przygotowuje konto magazynu do migracji.</span><span class="sxs-lookup"><span data-stu-id="6b965-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b965-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="6b965-136">-Profile</span></span>
<span data-ttu-id="6b965-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b965-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b965-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6b965-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b965-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b965-139">-StorageAccountName</span></span>
<span data-ttu-id="6b965-140">Określa nazwę konta magazynu, które jest migrowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b965-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b965-141">-Validate</span><span class="sxs-lookup"><span data-stu-id="6b965-141">-Validate</span></span>
<span data-ttu-id="6b965-142">Określa, że to polecenie cmdlet sprawdza poprawność konta magazynu do migracji.</span><span class="sxs-lookup"><span data-stu-id="6b965-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b965-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b965-143">CommonParameters</span></span>
<span data-ttu-id="6b965-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b965-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b965-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b965-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b965-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b965-146">INPUTS</span></span>

## <span data-ttu-id="6b965-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b965-147">OUTPUTS</span></span>

## <span data-ttu-id="6b965-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b965-148">NOTES</span></span>

## <span data-ttu-id="6b965-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b965-149">RELATED LINKS</span></span>

[<span data-ttu-id="6b965-150">Przenieś — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="6b965-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="6b965-151">Przenieś — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="6b965-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="6b965-152">Przenieś — AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="6b965-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="6b965-153">Przenieś — AzureService</span><span class="sxs-lookup"><span data-stu-id="6b965-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="6b965-154">Przenieś — AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6b965-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


