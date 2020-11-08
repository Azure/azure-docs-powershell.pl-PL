---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054541"
---
# <span data-ttu-id="c986f-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c986f-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="c986f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c986f-102">SYNOPSIS</span></span>
<span data-ttu-id="c986f-103">Pobiera mapowania obiektów magazynu odzyskiwania witryny dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="c986f-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="c986f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c986f-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c986f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c986f-105">DESCRIPTION</span></span>
<span data-ttu-id="c986f-106">Polecenie cmdlet **Get-AzureSiteRecoveryStorageMapping** Pobiera mapowania obiektów magazynu odzyskiwania witryny platformy Azure dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c986f-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c986f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c986f-107">EXAMPLES</span></span>

### <span data-ttu-id="c986f-108">Przykład 1: uzyskiwanie mapowania między obiektem magazynu a obiektem magazynu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="c986f-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="c986f-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="c986f-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="c986f-110">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="c986f-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="c986f-111">Drugie polecenie uzyskuje mapowanie między dwoma obiektami magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c986f-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="c986f-112">Polecenie Określa podstawowy serwer mapowania obiektów magazynu jako pierwszy element $Servers.</span><span class="sxs-lookup"><span data-stu-id="c986f-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="c986f-113">Polecenie Określa serwer obiektu przechowywania odzyskiwania jako drugi element $Servers.</span><span class="sxs-lookup"><span data-stu-id="c986f-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="c986f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c986f-114">PARAMETERS</span></span>

### <span data-ttu-id="c986f-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="c986f-115">-PrimaryServer</span></span>
<span data-ttu-id="c986f-116">Określa serwer podstawowy.</span><span class="sxs-lookup"><span data-stu-id="c986f-116">Specifies the primary server.</span></span>
<span data-ttu-id="c986f-117">Aby uzyskać serwer, użyj polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="c986f-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c986f-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c986f-118">-Profile</span></span>
<span data-ttu-id="c986f-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c986f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c986f-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c986f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c986f-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c986f-121">-RecoveryServer</span></span>
<span data-ttu-id="c986f-122">Określa serwer odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="c986f-122">Specifies the recovery server.</span></span>
<span data-ttu-id="c986f-123">Aby uzyskać serwer, użyj polecenie **Get-AzureSiteRecoveryServer**.</span><span class="sxs-lookup"><span data-stu-id="c986f-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c986f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c986f-124">CommonParameters</span></span>
<span data-ttu-id="c986f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c986f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c986f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c986f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c986f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c986f-127">INPUTS</span></span>

## <span data-ttu-id="c986f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c986f-128">OUTPUTS</span></span>

## <span data-ttu-id="c986f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c986f-129">NOTES</span></span>

## <span data-ttu-id="c986f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c986f-130">RELATED LINKS</span></span>

[<span data-ttu-id="c986f-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c986f-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="c986f-132">Nowe — AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c986f-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="c986f-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="c986f-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


