---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554214"
---
# <span data-ttu-id="7a93c-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7a93c-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="7a93c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a93c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a93c-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="7a93c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a93c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a93c-104">SYNTAX</span></span>

### <span data-ttu-id="7a93c-105">Parametr ustawiony dla parametrów pól (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7a93c-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a93c-106">Zestaw parametrów dla parametrów obiektu</span><span class="sxs-lookup"><span data-stu-id="7a93c-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a93c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a93c-107">DESCRIPTION</span></span>
<span data-ttu-id="7a93c-108">{{Wpisz opis}}</span><span class="sxs-lookup"><span data-stu-id="7a93c-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7a93c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a93c-109">EXAMPLES</span></span>

### <span data-ttu-id="7a93c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a93c-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7a93c-111">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="7a93c-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7a93c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a93c-112">PARAMETERS</span></span>

### <span data-ttu-id="7a93c-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7a93c-113">-CdnProfile</span></span>
<span data-ttu-id="7a93c-114">Obiekt profilu usługi Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="7a93c-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a93c-115">-Refilename</span><span class="sxs-lookup"><span data-stu-id="7a93c-115">-ProfileName</span></span>
<span data-ttu-id="7a93c-116">Nazwa profilu.</span><span class="sxs-lookup"><span data-stu-id="7a93c-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a93c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a93c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a93c-118">Grupa zasobów, do której należy profil.</span><span class="sxs-lookup"><span data-stu-id="7a93c-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a93c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a93c-119">-DefaultProfile</span></span>
<span data-ttu-id="7a93c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a93c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a93c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a93c-121">CommonParameters</span></span>
<span data-ttu-id="7a93c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a93c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a93c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a93c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a93c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a93c-124">INPUTS</span></span>

### <span data-ttu-id="7a93c-125">Microsoft. Azure. Commands. CDN. models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7a93c-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7a93c-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a93c-126">OUTPUTS</span></span>

### <span data-ttu-id="7a93c-127">Microsoft. Azure. Commands. CDN. modele. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7a93c-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="7a93c-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a93c-128">NOTES</span></span>

## <span data-ttu-id="7a93c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a93c-129">RELATED LINKS</span></span>

