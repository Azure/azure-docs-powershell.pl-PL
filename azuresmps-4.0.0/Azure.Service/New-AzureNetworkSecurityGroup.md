---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054876"
---
# <span data-ttu-id="a6721-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6721-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="a6721-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6721-102">SYNOPSIS</span></span>
<span data-ttu-id="a6721-103">Tworzy grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="a6721-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="a6721-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6721-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6721-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6721-105">DESCRIPTION</span></span>
<span data-ttu-id="a6721-106">Polecenie cmdlet **New-AzureNetworkSecurityGroup** tworzy grupę zabezpieczeń sieci Azure w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a6721-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="a6721-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6721-107">EXAMPLES</span></span>

## <span data-ttu-id="a6721-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6721-108">PARAMETERS</span></span>

### <span data-ttu-id="a6721-109">-Label</span><span class="sxs-lookup"><span data-stu-id="a6721-109">-Label</span></span>
<span data-ttu-id="a6721-110">Określa opis nowej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a6721-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6721-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a6721-111">-Location</span></span>
<span data-ttu-id="a6721-112">Określa lokalizację platformy Azure, w której to polecenie cmdlet tworzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a6721-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="a6721-113">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="a6721-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="a6721-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a6721-114">-Name</span></span>
<span data-ttu-id="a6721-115">Określa nazwę nowej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a6721-115">Specifies a name for the new network security group.</span></span>

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

### <span data-ttu-id="a6721-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="a6721-116">-Profile</span></span>
<span data-ttu-id="a6721-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6721-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6721-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a6721-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6721-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6721-119">CommonParameters</span></span>
<span data-ttu-id="a6721-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6721-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6721-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6721-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6721-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6721-122">INPUTS</span></span>

## <span data-ttu-id="a6721-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6721-123">OUTPUTS</span></span>

## <span data-ttu-id="a6721-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6721-124">NOTES</span></span>

## <span data-ttu-id="a6721-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6721-125">RELATED LINKS</span></span>

[<span data-ttu-id="a6721-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a6721-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


