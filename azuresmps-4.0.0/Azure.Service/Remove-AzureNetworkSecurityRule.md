---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054835"
---
# <span data-ttu-id="27572-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="27572-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="27572-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27572-102">SYNOPSIS</span></span>
<span data-ttu-id="27572-103">Usuwa regułę zabezpieczeń sieci z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="27572-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="27572-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27572-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27572-105">Opis</span><span class="sxs-lookup"><span data-stu-id="27572-105">DESCRIPTION</span></span>
<span data-ttu-id="27572-106">Polecenie cmdlet **Remove-AzureNetworkSecurityRule** usuwa regułę zabezpieczeń sieci Azure z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="27572-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="27572-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27572-107">EXAMPLES</span></span>

## <span data-ttu-id="27572-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27572-108">PARAMETERS</span></span>

### <span data-ttu-id="27572-109">-Force</span><span class="sxs-lookup"><span data-stu-id="27572-109">-Force</span></span>
<span data-ttu-id="27572-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="27572-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27572-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="27572-111">-Name</span></span>
<span data-ttu-id="27572-112">Określa nazwę reguły zabezpieczeń sieci, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27572-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="27572-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27572-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="27572-114">Określa grupę zabezpieczeń sieci, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="27572-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="27572-115">Aby uzyskać obiekt **INetworkSecurityGroup** , użyj polecenia cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="27572-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27572-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="27572-116">-Profile</span></span>
<span data-ttu-id="27572-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27572-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="27572-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="27572-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27572-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27572-119">CommonParameters</span></span>
<span data-ttu-id="27572-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27572-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27572-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27572-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27572-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27572-122">INPUTS</span></span>

## <span data-ttu-id="27572-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27572-123">OUTPUTS</span></span>

## <span data-ttu-id="27572-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27572-124">NOTES</span></span>

## <span data-ttu-id="27572-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27572-125">RELATED LINKS</span></span>

[<span data-ttu-id="27572-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="27572-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


