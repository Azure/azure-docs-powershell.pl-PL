---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219563"
---
# <span data-ttu-id="0ec10-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0ec10-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="0ec10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ec10-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec10-103">Pobiera tablicę z identyfikatorem prywatnego linku, który można połączyć z prywatnym punktem końcowym z opcją automatycznie zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="0ec10-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="0ec10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ec10-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ec10-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ec10-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec10-106">Polecenie **Get-AzAutoApprovedPrivateLinkService** pobiera tablicę identyfikatora usługi linku prywatnego, która może być połączona z prywatnym punktem końcowym z opcją automatycznie zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="0ec10-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="0ec10-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ec10-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec10-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ec10-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="0ec10-109">W tym przykładzie zwrócono tablicę z identyfikatorem prywatnego linku, który można połączyć z prywatnym punktem końcowym z opcją automatycznie zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="0ec10-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="0ec10-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ec10-110">PARAMETERS</span></span>

### <span data-ttu-id="0ec10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec10-111">-DefaultProfile</span></span>
<span data-ttu-id="0ec10-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ec10-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ec10-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0ec10-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec10-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec10-114">-ResourceGroupName</span></span>
<span data-ttu-id="0ec10-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ec10-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec10-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec10-116">CommonParameters</span></span>
<span data-ttu-id="0ec10-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec10-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec10-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ec10-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec10-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ec10-119">INPUTS</span></span>

### <span data-ttu-id="0ec10-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0ec10-120">None</span></span>

## <span data-ttu-id="0ec10-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ec10-121">OUTPUTS</span></span>

### <span data-ttu-id="0ec10-122">Microsoft. Azure. Commands. Network. models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0ec10-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="0ec10-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ec10-123">NOTES</span></span>

## <span data-ttu-id="0ec10-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ec10-124">RELATED LINKS</span></span>
