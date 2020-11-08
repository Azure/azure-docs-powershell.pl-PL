---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055120"
---
# <span data-ttu-id="b165c-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b165c-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="b165c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b165c-102">SYNOPSIS</span></span>
<span data-ttu-id="b165c-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b165c-103">Deletes a network security group.</span></span>

## <span data-ttu-id="b165c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b165c-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b165c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b165c-105">DESCRIPTION</span></span>
<span data-ttu-id="b165c-106">Polecenie cmdlet **Remove-AzureNetworkSecurityGroup** usuwa grupę zabezpieczeń sieci Azure z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b165c-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="b165c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b165c-107">EXAMPLES</span></span>

## <span data-ttu-id="b165c-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b165c-108">PARAMETERS</span></span>

### <span data-ttu-id="b165c-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b165c-109">-Force</span></span>
<span data-ttu-id="b165c-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b165c-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b165c-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b165c-111">-Name</span></span>
<span data-ttu-id="b165c-112">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="b165c-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b165c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b165c-113">-PassThru</span></span>
<span data-ttu-id="b165c-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b165c-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b165c-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b165c-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b165c-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="b165c-116">-Profile</span></span>
<span data-ttu-id="b165c-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b165c-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b165c-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b165c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b165c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b165c-119">CommonParameters</span></span>
<span data-ttu-id="b165c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b165c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b165c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b165c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b165c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b165c-122">INPUTS</span></span>

## <span data-ttu-id="b165c-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b165c-123">OUTPUTS</span></span>

## <span data-ttu-id="b165c-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b165c-124">NOTES</span></span>

## <span data-ttu-id="b165c-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b165c-125">RELATED LINKS</span></span>

[<span data-ttu-id="b165c-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b165c-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b165c-127">Nowe — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b165c-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


