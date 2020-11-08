---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054858"
---
# <span data-ttu-id="bf0ed-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="bf0ed-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="bf0ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf0ed-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0ed-103">Tworzy witrynę odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="bf0ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf0ed-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf0ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf0ed-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0ed-106">Polecenie cmdlet **New-AzureSiteRecoverySite** tworzy witrynę Azure Site Recovery w bieżącym magazynie.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="bf0ed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf0ed-107">EXAMPLES</span></span>

### <span data-ttu-id="bf0ed-108">Przykład 1. Tworzenie witryny odzyskiwania witryny</span><span class="sxs-lookup"><span data-stu-id="bf0ed-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="bf0ed-109">To polecenie tworzy witrynę odzyskiwania witryny o nazwie RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="bf0ed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf0ed-110">PARAMETERS</span></span>

### <span data-ttu-id="bf0ed-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf0ed-111">-Name</span></span>
<span data-ttu-id="bf0ed-112">Określa nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-112">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="bf0ed-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="bf0ed-113">-Profile</span></span>
<span data-ttu-id="bf0ed-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf0ed-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf0ed-116">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="bf0ed-116">-Vault</span></span>
<span data-ttu-id="bf0ed-117">Określa magazyn, dla którego ma zostać utworzona witryna.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="bf0ed-118">Aby uzyskać obiekt **ASRVault** , użyj polecenia cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="bf0ed-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="bf0ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0ed-119">CommonParameters</span></span>
<span data-ttu-id="bf0ed-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0ed-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0ed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0ed-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf0ed-122">INPUTS</span></span>

## <span data-ttu-id="bf0ed-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf0ed-123">OUTPUTS</span></span>

## <span data-ttu-id="bf0ed-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf0ed-124">NOTES</span></span>

## <span data-ttu-id="bf0ed-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf0ed-125">RELATED LINKS</span></span>

[<span data-ttu-id="bf0ed-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="bf0ed-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="bf0ed-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="bf0ed-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


