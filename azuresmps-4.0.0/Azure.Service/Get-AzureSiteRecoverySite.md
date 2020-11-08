---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054543"
---
# <span data-ttu-id="c08c3-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="c08c3-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="c08c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c08c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c08c3-103">Pobiera witryny Hyper-V z magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="c08c3-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="c08c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c08c3-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c08c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c08c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c08c3-106">Polecenie cmdlet **Get-AzureSiteRecoverySite** pobiera witryny Hyper-V w magazynie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="c08c3-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c08c3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c08c3-107">EXAMPLES</span></span>

### <span data-ttu-id="c08c3-108">Przykład 1: pobieranie witryn odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="c08c3-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="c08c3-109">To polecenie pobiera witryny odzyskiwania dla bieżącego magazynu.</span><span class="sxs-lookup"><span data-stu-id="c08c3-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="c08c3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c08c3-110">PARAMETERS</span></span>

### <span data-ttu-id="c08c3-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="c08c3-111">-Profile</span></span>
<span data-ttu-id="c08c3-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c08c3-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c08c3-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c08c3-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c08c3-114">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="c08c3-114">-Vault</span></span>
<span data-ttu-id="c08c3-115">Określa magazyn, dla którego należy pobrać witryny.</span><span class="sxs-lookup"><span data-stu-id="c08c3-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="c08c3-116">Aby uzyskać obiekt **ASRVault** , użyj polecenia cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="c08c3-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c08c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08c3-117">CommonParameters</span></span>
<span data-ttu-id="c08c3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c08c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08c3-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08c3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08c3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c08c3-120">INPUTS</span></span>

## <span data-ttu-id="c08c3-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c08c3-121">OUTPUTS</span></span>

## <span data-ttu-id="c08c3-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c08c3-122">NOTES</span></span>

## <span data-ttu-id="c08c3-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c08c3-123">RELATED LINKS</span></span>

[<span data-ttu-id="c08c3-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="c08c3-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="c08c3-125">Nowe — AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="c08c3-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


