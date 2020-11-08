---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054542"
---
# <span data-ttu-id="d72a8-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="d72a8-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="d72a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d72a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d72a8-103">Pobiera magazyny odzyskiwania witryny dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="d72a8-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="d72a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d72a8-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d72a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d72a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d72a8-106">Polecenie cmdlet **Get-AzureSiteRecoveryStorage** pobiera magazyny odzyskiwania witryny platformy Azure dla bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d72a8-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d72a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d72a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d72a8-108">Przykład 1: pobieranie magazynu odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="d72a8-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="d72a8-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="d72a8-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="d72a8-110">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="d72a8-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="d72a8-111">Drugie polecenie pobiera magazyn odzyskiwania witryny dla pierwszego serwera w tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="d72a8-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="d72a8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d72a8-112">PARAMETERS</span></span>

### <span data-ttu-id="d72a8-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="d72a8-113">-Profile</span></span>
<span data-ttu-id="d72a8-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d72a8-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d72a8-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d72a8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d72a8-116">-Server</span><span class="sxs-lookup"><span data-stu-id="d72a8-116">-Server</span></span>
<span data-ttu-id="d72a8-117">Określa serwer magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d72a8-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="d72a8-118">Aby uzyskać obiekt **ASRServer** , użyj polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="d72a8-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72a8-119">CommonParameters</span></span>
<span data-ttu-id="d72a8-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d72a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72a8-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72a8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72a8-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d72a8-122">INPUTS</span></span>

## <span data-ttu-id="d72a8-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d72a8-123">OUTPUTS</span></span>

## <span data-ttu-id="d72a8-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d72a8-124">NOTES</span></span>

## <span data-ttu-id="d72a8-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d72a8-125">RELATED LINKS</span></span>

[<span data-ttu-id="d72a8-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="d72a8-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


