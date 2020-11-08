---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054558"
---
# <span data-ttu-id="88dd1-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="88dd1-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="88dd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="88dd1-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="88dd1-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="88dd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88dd1-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="88dd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="88dd1-106">Polecenie cmdlet **Get-AzureSiteRecoveryNetwork** pobiera informacje o sieciach usługi Azure Site Recovery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="88dd1-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="88dd1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88dd1-107">EXAMPLES</span></span>

### <span data-ttu-id="88dd1-108">Przykład 1: pobieranie sieci odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="88dd1-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="88dd1-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="88dd1-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="88dd1-110">Polecenie zapisuje serwery odzyskiwania witryny w zmiennej tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="88dd1-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="88dd1-111">Drugie polecenie pobiera sieć odzyskiwania witryny dla pierwszego serwera w tablicy $Servers.</span><span class="sxs-lookup"><span data-stu-id="88dd1-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="88dd1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88dd1-112">PARAMETERS</span></span>

### <span data-ttu-id="88dd1-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="88dd1-113">-Profile</span></span>
<span data-ttu-id="88dd1-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88dd1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88dd1-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="88dd1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88dd1-116">-Server</span><span class="sxs-lookup"><span data-stu-id="88dd1-116">-Server</span></span>
<span data-ttu-id="88dd1-117">Określa serwer odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="88dd1-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="88dd1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dd1-118">CommonParameters</span></span>
<span data-ttu-id="88dd1-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dd1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dd1-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dd1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dd1-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88dd1-121">INPUTS</span></span>

## <span data-ttu-id="88dd1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88dd1-122">OUTPUTS</span></span>

## <span data-ttu-id="88dd1-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88dd1-123">NOTES</span></span>

## <span data-ttu-id="88dd1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88dd1-124">RELATED LINKS</span></span>

[<span data-ttu-id="88dd1-125">Polecenia cmdlet usług Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="88dd1-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


