---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054940"
---
# <span data-ttu-id="8afb4-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8afb4-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="8afb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8afb4-102">SYNOPSIS</span></span>
<span data-ttu-id="8afb4-103">Tworzy magazyn usług odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="8afb4-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="8afb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8afb4-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8afb4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8afb4-105">DESCRIPTION</span></span>
<span data-ttu-id="8afb4-106">Polecenie cmdlet **New-AzureSiteRecoveryVault** tworzy magazyn usług Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8afb4-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="8afb4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8afb4-107">EXAMPLES</span></span>

### <span data-ttu-id="8afb4-108">Przykład 1. Tworzenie magazynu</span><span class="sxs-lookup"><span data-stu-id="8afb4-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="8afb4-109">To polecenie tworzy magazyn o nazwie ContosoVault w zachodniej lokalizacji w Stanach Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="8afb4-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="8afb4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8afb4-110">PARAMETERS</span></span>

### <span data-ttu-id="8afb4-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8afb4-111">-Location</span></span>
<span data-ttu-id="8afb4-112">Określa lokalizację geograficzną.</span><span class="sxs-lookup"><span data-stu-id="8afb4-112">Specifies the geographical location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afb4-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8afb4-113">-Name</span></span>
<span data-ttu-id="8afb4-114">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="8afb4-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afb4-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="8afb4-115">-Profile</span></span>
<span data-ttu-id="8afb4-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8afb4-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8afb4-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8afb4-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8afb4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afb4-118">CommonParameters</span></span>
<span data-ttu-id="8afb4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afb4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afb4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afb4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afb4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8afb4-121">INPUTS</span></span>

## <span data-ttu-id="8afb4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8afb4-122">OUTPUTS</span></span>

## <span data-ttu-id="8afb4-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8afb4-123">NOTES</span></span>

## <span data-ttu-id="8afb4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8afb4-124">RELATED LINKS</span></span>

[<span data-ttu-id="8afb4-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8afb4-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


