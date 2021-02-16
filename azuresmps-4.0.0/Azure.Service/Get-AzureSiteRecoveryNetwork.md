---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411589"
---
# <span data-ttu-id="82fe7-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="82fe7-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="82fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="82fe7-103">Pobiera informacje o sieciach zarządzanych przez odzyskiwanie witryny dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="82fe7-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="82fe7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="82fe7-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="82fe7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="82fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="82fe7-106">Polecenie **cmdlet Get-AzureSiteRecoveryNetwork** pobiera informacje o sieciach Azure Site Recovery dla bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="82fe7-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="82fe7-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="82fe7-107">EXAMPLES</span></span>

### <span data-ttu-id="82fe7-108">Przykład 1. Uzyskiwanie sieci odzyskiwania witryn</span><span class="sxs-lookup"><span data-stu-id="82fe7-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="82fe7-109">Pierwsze polecenie cmdlet pobiera serwery dla bieżącego magazynu usługi Azure Site Recovery przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryServer.**</span><span class="sxs-lookup"><span data-stu-id="82fe7-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="82fe7-110">To polecenie przechowuje serwery odzyskiwania witryn w $Servers tablicowej.</span><span class="sxs-lookup"><span data-stu-id="82fe7-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="82fe7-111">Drugie polecenie pobiera sieć odzyskiwania witryny dla pierwszego serwera w $Servers tablicy.</span><span class="sxs-lookup"><span data-stu-id="82fe7-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="82fe7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82fe7-112">PARAMETERS</span></span>

### <span data-ttu-id="82fe7-113">— Profil</span><span class="sxs-lookup"><span data-stu-id="82fe7-113">-Profile</span></span>
<span data-ttu-id="82fe7-114">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82fe7-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82fe7-115">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="82fe7-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82fe7-116">— Serwer</span><span class="sxs-lookup"><span data-stu-id="82fe7-116">-Server</span></span>
<span data-ttu-id="82fe7-117">Określa serwer odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="82fe7-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="82fe7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fe7-118">CommonParameters</span></span>
<span data-ttu-id="82fe7-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82fe7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fe7-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82fe7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fe7-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82fe7-121">INPUTS</span></span>

## <span data-ttu-id="82fe7-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82fe7-122">OUTPUTS</span></span>

## <span data-ttu-id="82fe7-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="82fe7-123">NOTES</span></span>

## <span data-ttu-id="82fe7-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82fe7-124">RELATED LINKS</span></span>




