---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054941"
---
# <span data-ttu-id="59848-101">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="59848-101">New-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="59848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59848-102">SYNOPSIS</span></span>
<span data-ttu-id="59848-103">Tworzy mapowanie między obiektem magazynu platformy Azure a obiektem magazynu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59848-103">Creates a mapping between an Azure Storage object and recovery Storage object.</span></span>

## <span data-ttu-id="59848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59848-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="59848-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59848-105">DESCRIPTION</span></span>
<span data-ttu-id="59848-106">Polecenie cmdlet **New-AzureSiteRecoveryStorageMapping** tworzy mapowanie między obiektem magazynu podstawowego zarządzania witryną Azure i obiektem odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59848-106">The **New-AzureSiteRecoveryStorageMapping** cmdlet creates a mapping between an Azure Site Recovery managed primary Azure Storage object and a recovery Storage object.</span></span>

## <span data-ttu-id="59848-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59848-107">EXAMPLES</span></span>

### <span data-ttu-id="59848-108">Przykład 1. Tworzenie mapowania między obiektem magazynu a obiektem magazynu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="59848-108">Example 1: Create a mapping between a storage object and a recovery storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

<span data-ttu-id="59848-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="59848-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="59848-110">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="59848-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="59848-111">Drugie polecenie pobiera magazyn odzyskiwania witryny dla pierwszego serwera w tablicy $Servers, a następnie przechowuje go w $Storages.</span><span class="sxs-lookup"><span data-stu-id="59848-111">The second command gets the site recovery storage for the first server in the $Servers array, and then stores it in the $Storages.</span></span>

<span data-ttu-id="59848-112">Ostatnie polecenie tworzy mapowanie między siecią podstawową a siecią odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59848-112">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="59848-113">Polecenie Określa podstawowy obiekt magazynu jako pierwszy element $Storages.</span><span class="sxs-lookup"><span data-stu-id="59848-113">The command specifies the primary Storage object as the first element of $Storages.</span></span>
<span data-ttu-id="59848-114">Polecenie określa obiekt magazynu odzyskiwania jako drugi element $Storages.</span><span class="sxs-lookup"><span data-stu-id="59848-114">The command specifies the recovery Storage object as the second element of $Storages.</span></span>

## <span data-ttu-id="59848-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59848-115">PARAMETERS</span></span>

### <span data-ttu-id="59848-116">-PrimaryStorage</span><span class="sxs-lookup"><span data-stu-id="59848-116">-PrimaryStorage</span></span>
<span data-ttu-id="59848-117">Określa podstawowy magazyn do zamapowania na magazyn odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59848-117">Specifies the primary Storage to map to the recovery Storage.</span></span>
<span data-ttu-id="59848-118">Aby uzyskać obiekt **ASRStorage** , użyj polecenia cmdlet Get-AzureSiteRecoveryStorage.</span><span class="sxs-lookup"><span data-stu-id="59848-118">To obtain an **ASRStorage** object, use the Get-AzureSiteRecoveryStorage cmdlet.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59848-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="59848-119">-Profile</span></span>
<span data-ttu-id="59848-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59848-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="59848-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="59848-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="59848-122">-RecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="59848-122">-RecoveryStorage</span></span>
<span data-ttu-id="59848-123">Określa obiekt magazynu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="59848-123">Specifies the recovery Storage object.</span></span>
<span data-ttu-id="59848-124">To polecenie cmdlet mapuje obiekt magazynu podstawowego do obiektu magazynu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="59848-124">This cmdlet maps the primary Storage object to the Storage object that this parameter specifies.</span></span>
<span data-ttu-id="59848-125">Aby uzyskać obiekt **ASRStorage** , użyj polecenie **Get-AzureSiteRecoveryStorage**.</span><span class="sxs-lookup"><span data-stu-id="59848-125">To obtain an **ASRStorage** object, use **Get-AzureSiteRecoveryStorage**.</span></span>

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59848-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59848-126">CommonParameters</span></span>
<span data-ttu-id="59848-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59848-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59848-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59848-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59848-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59848-129">INPUTS</span></span>

## <span data-ttu-id="59848-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59848-130">OUTPUTS</span></span>

## <span data-ttu-id="59848-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59848-131">NOTES</span></span>

## <span data-ttu-id="59848-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59848-132">RELATED LINKS</span></span>

[<span data-ttu-id="59848-133">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="59848-133">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)

[<span data-ttu-id="59848-134">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="59848-134">Get-AzureSiteRecoveryStorageMapping</span></span>](./Get-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="59848-135">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="59848-135">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


