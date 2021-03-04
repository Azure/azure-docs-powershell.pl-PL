---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: dbc21a337263bb0e509188d472e4ff984e22322b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951745"
---
# <span data-ttu-id="dad1f-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="dad1f-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="dad1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad1f-102">SYNOPSIS</span></span>
<span data-ttu-id="dad1f-103">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="dad1f-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="dad1f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dad1f-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dad1f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dad1f-105">DESCRIPTION</span></span>
<span data-ttu-id="dad1f-106">Sprawdza, czy nazwa domeny w strefie cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="dad1f-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="dad1f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dad1f-107">EXAMPLES</span></span>

### <span data-ttu-id="dad1f-108">Przykład 1. Sprawdź, czy contoso.westus.cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="dad1f-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="dad1f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dad1f-109">PARAMETERS</span></span>

### <span data-ttu-id="dad1f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad1f-110">-DefaultProfile</span></span>
<span data-ttu-id="dad1f-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dad1f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dad1f-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="dad1f-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad1f-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dad1f-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad1f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad1f-114">CommonParameters</span></span>
<span data-ttu-id="dad1f-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad1f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad1f-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad1f-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad1f-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dad1f-117">INPUTS</span></span>

### <span data-ttu-id="dad1f-118">Brak</span><span class="sxs-lookup"><span data-stu-id="dad1f-118">None</span></span>

## <span data-ttu-id="dad1f-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dad1f-119">OUTPUTS</span></span>

### <span data-ttu-id="dad1f-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dad1f-120">System.Boolean</span></span>

## <span data-ttu-id="dad1f-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dad1f-121">NOTES</span></span>

## <span data-ttu-id="dad1f-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dad1f-122">RELATED LINKS</span></span>
