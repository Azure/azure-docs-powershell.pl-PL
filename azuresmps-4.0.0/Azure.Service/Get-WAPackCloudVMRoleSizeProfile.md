---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055474"
---
# <span data-ttu-id="63617-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="63617-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="63617-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63617-102">SYNOPSIS</span></span>
<span data-ttu-id="63617-103">Pobiera obiekty profilu rozmiaru roli maszyny wirtualnej chmury.</span><span class="sxs-lookup"><span data-stu-id="63617-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="63617-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63617-104">SYNTAX</span></span>

### <span data-ttu-id="63617-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="63617-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63617-106">Odname</span><span class="sxs-lookup"><span data-stu-id="63617-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63617-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63617-107">DESCRIPTION</span></span>
<span data-ttu-id="63617-108">Polecenie cmdlet **Get-WAPackCloudVMRoleSizeProfile** Pobiera obiekty profilu rozmiaru roli maszyny wirtualnej w chmurze dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="63617-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="63617-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63617-109">EXAMPLES</span></span>

### <span data-ttu-id="63617-110">Przykład 1: uzyskiwanie profilu rozmiaru roli maszyny wirtualnej w chmurze przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="63617-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="63617-111">To polecenie pobiera profil rozmiaru o nazwie małe.</span><span class="sxs-lookup"><span data-stu-id="63617-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="63617-112">Przykład 2: uzyskiwanie wszystkich profilów rozmiaru roli maszyny wirtualnej w chmurze</span><span class="sxs-lookup"><span data-stu-id="63617-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="63617-113">To polecenie pobiera wszystkie profile rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="63617-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="63617-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63617-114">PARAMETERS</span></span>

### <span data-ttu-id="63617-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63617-115">-Name</span></span>
<span data-ttu-id="63617-116">Określa nazwę profilu rozmiaru roli maszyny wirtualnej w chmurze.</span><span class="sxs-lookup"><span data-stu-id="63617-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63617-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="63617-117">-Profile</span></span>
<span data-ttu-id="63617-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63617-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63617-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="63617-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63617-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63617-120">CommonParameters</span></span>
<span data-ttu-id="63617-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63617-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63617-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63617-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63617-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63617-123">INPUTS</span></span>

## <span data-ttu-id="63617-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63617-124">OUTPUTS</span></span>

## <span data-ttu-id="63617-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63617-125">NOTES</span></span>

## <span data-ttu-id="63617-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63617-126">RELATED LINKS</span></span>

[<span data-ttu-id="63617-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="63617-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


