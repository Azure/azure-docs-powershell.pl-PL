---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055531"
---
# <span data-ttu-id="fe9d7-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fe9d7-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="fe9d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9d7-103">Pobiera magazyny odzyskiwania witryny z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="fe9d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe9d7-104">SYNTAX</span></span>

### <span data-ttu-id="fe9d7-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fe9d7-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fe9d7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fe9d7-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe9d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe9d7-107">DESCRIPTION</span></span>
<span data-ttu-id="fe9d7-108">Polecenie cmdlet **Get-AzureSiteRecoveryVault** pobiera listę magazynów odzyskiwania witryny usługi Azure lub określonego magazynu do odtworzenia witryny z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="fe9d7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe9d7-109">EXAMPLES</span></span>

### <span data-ttu-id="fe9d7-110">Przykład 1: uzyskiwanie aktywnego magazynu</span><span class="sxs-lookup"><span data-stu-id="fe9d7-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="fe9d7-111">To polecenie pobiera aktywny magazyn usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fe9d7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe9d7-112">PARAMETERS</span></span>

### <span data-ttu-id="fe9d7-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe9d7-113">-Name</span></span>
<span data-ttu-id="fe9d7-114">Określa nazwę magazynu, który należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-114">Specifies the name of the vault to get.</span></span>

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

### <span data-ttu-id="fe9d7-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="fe9d7-115">-Profile</span></span>
<span data-ttu-id="fe9d7-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe9d7-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe9d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9d7-118">CommonParameters</span></span>
<span data-ttu-id="fe9d7-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9d7-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9d7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9d7-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe9d7-121">INPUTS</span></span>

## <span data-ttu-id="fe9d7-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe9d7-122">OUTPUTS</span></span>

## <span data-ttu-id="fe9d7-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe9d7-123">NOTES</span></span>

## <span data-ttu-id="fe9d7-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe9d7-124">RELATED LINKS</span></span>

[<span data-ttu-id="fe9d7-125">Nowe — AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="fe9d7-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


