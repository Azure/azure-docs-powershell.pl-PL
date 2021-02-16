---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412286"
---
# <span data-ttu-id="b53fe-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b53fe-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="b53fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b53fe-102">SYNOPSIS</span></span>
<span data-ttu-id="b53fe-103">Pobiera serwery odzyskiwania witryn, które zarejestrły magazyn odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b53fe-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="b53fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b53fe-104">SYNTAX</span></span>

### <span data-ttu-id="b53fe-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b53fe-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b53fe-106">ById</span><span class="sxs-lookup"><span data-stu-id="b53fe-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b53fe-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b53fe-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b53fe-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b53fe-108">DESCRIPTION</span></span>
<span data-ttu-id="b53fe-109">Polecenie **cmdlet Get-AzureSiteRecoveryServer** pobiera informacje o serwerach azure site recovery zarejestrowanych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b53fe-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="b53fe-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b53fe-110">EXAMPLES</span></span>

### <span data-ttu-id="b53fe-111">Przykład 1. Uzyskiwanie informacji o serwerze odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="b53fe-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="b53fe-112">To polecenie pobiera informacje o serwerze Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b53fe-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="b53fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b53fe-113">PARAMETERS</span></span>

### <span data-ttu-id="b53fe-114">— Id</span><span class="sxs-lookup"><span data-stu-id="b53fe-114">-Id</span></span>
<span data-ttu-id="b53fe-115">Określa identyfikator serwera.</span><span class="sxs-lookup"><span data-stu-id="b53fe-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b53fe-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b53fe-116">-Name</span></span>
<span data-ttu-id="b53fe-117">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="b53fe-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b53fe-118">— Profil</span><span class="sxs-lookup"><span data-stu-id="b53fe-118">-Profile</span></span>
<span data-ttu-id="b53fe-119">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53fe-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b53fe-120">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="b53fe-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b53fe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53fe-121">CommonParameters</span></span>
<span data-ttu-id="b53fe-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53fe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53fe-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53fe-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53fe-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b53fe-124">INPUTS</span></span>

## <span data-ttu-id="b53fe-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b53fe-125">OUTPUTS</span></span>

## <span data-ttu-id="b53fe-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b53fe-126">NOTES</span></span>

## <span data-ttu-id="b53fe-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b53fe-127">RELATED LINKS</span></span>




