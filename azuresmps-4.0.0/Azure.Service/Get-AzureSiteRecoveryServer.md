---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054546"
---
# <span data-ttu-id="b872e-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b872e-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="b872e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b872e-102">SYNOPSIS</span></span>
<span data-ttu-id="b872e-103">Pobiera serwery odzyskiwania witryny zarejestrowane w magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b872e-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="b872e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b872e-104">SYNTAX</span></span>

### <span data-ttu-id="b872e-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b872e-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b872e-106">ById</span><span class="sxs-lookup"><span data-stu-id="b872e-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b872e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b872e-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b872e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b872e-108">DESCRIPTION</span></span>
<span data-ttu-id="b872e-109">Polecenie cmdlet **Get-AzureSiteRecoveryServer** pobiera informacje o serwerach usługi Azure Site Recovery zarejestrowanych w bieżącym magazynie odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b872e-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="b872e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b872e-110">EXAMPLES</span></span>

### <span data-ttu-id="b872e-111">Przykład 1: uzyskiwanie informacji o serwerze odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="b872e-111">Example 1: Get information about a Site Recovery server</span></span>
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

<span data-ttu-id="b872e-112">To polecenie pobiera informacje o serwerze usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b872e-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="b872e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b872e-113">PARAMETERS</span></span>

### <span data-ttu-id="b872e-114">-ID</span><span class="sxs-lookup"><span data-stu-id="b872e-114">-Id</span></span>
<span data-ttu-id="b872e-115">Określa identyfikator serwera.</span><span class="sxs-lookup"><span data-stu-id="b872e-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="b872e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b872e-116">-Name</span></span>
<span data-ttu-id="b872e-117">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="b872e-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="b872e-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="b872e-118">-Profile</span></span>
<span data-ttu-id="b872e-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b872e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b872e-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b872e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b872e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b872e-121">CommonParameters</span></span>
<span data-ttu-id="b872e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b872e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b872e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b872e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b872e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b872e-124">INPUTS</span></span>

## <span data-ttu-id="b872e-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b872e-125">OUTPUTS</span></span>

## <span data-ttu-id="b872e-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b872e-126">NOTES</span></span>

## <span data-ttu-id="b872e-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b872e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b872e-128">Polecenia cmdlet usług Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="b872e-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


