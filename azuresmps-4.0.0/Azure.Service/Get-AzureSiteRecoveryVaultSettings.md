---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055532"
---
# <span data-ttu-id="b81a0-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b81a0-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="b81a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b81a0-102">SYNOPSIS</span></span>
<span data-ttu-id="b81a0-103">Pobiera ustawienia magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="b81a0-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="b81a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b81a0-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b81a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b81a0-105">DESCRIPTION</span></span>
<span data-ttu-id="b81a0-106">Polecenie cmdlet **Get-AzureSiteRecoveryVaultSettings** pobiera ustawienia dotyczące bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b81a0-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b81a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b81a0-107">EXAMPLES</span></span>

### <span data-ttu-id="b81a0-108">Przykład 1: uzyskiwanie informacji o ustawieniach</span><span class="sxs-lookup"><span data-stu-id="b81a0-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="b81a0-109">To polecenie pobiera informacje o ustawieniach bieżącego magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b81a0-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b81a0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b81a0-110">PARAMETERS</span></span>

### <span data-ttu-id="b81a0-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="b81a0-111">-Profile</span></span>
<span data-ttu-id="b81a0-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b81a0-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b81a0-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b81a0-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b81a0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81a0-114">CommonParameters</span></span>
<span data-ttu-id="b81a0-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b81a0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81a0-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b81a0-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81a0-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b81a0-117">INPUTS</span></span>

## <span data-ttu-id="b81a0-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b81a0-118">OUTPUTS</span></span>

## <span data-ttu-id="b81a0-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b81a0-119">NOTES</span></span>

## <span data-ttu-id="b81a0-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b81a0-120">RELATED LINKS</span></span>

[<span data-ttu-id="b81a0-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b81a0-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="b81a0-122">Import — AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b81a0-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


