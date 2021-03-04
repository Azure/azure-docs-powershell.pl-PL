---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951713"
---
# <span data-ttu-id="f6327-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f6327-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="f6327-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6327-102">SYNOPSIS</span></span>
<span data-ttu-id="f6327-103">**Test-AzPrivateLinkServiceVisibility** sprawdza, czy prywatna usługa linków jest widoczna do bieżącego użycia.</span><span class="sxs-lookup"><span data-stu-id="f6327-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="f6327-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6327-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6327-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6327-105">DESCRIPTION</span></span>
<span data-ttu-id="f6327-106">Sprawdzanie, czy prywatna usługa linków jest widoczna do bieżącego użytku.</span><span class="sxs-lookup"><span data-stu-id="f6327-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="f6327-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6327-107">EXAMPLES</span></span>

### <span data-ttu-id="f6327-108">Przykład 1. Sprawdź, czy contoso.cloudapp.azure.com jest dostępna do użycia.</span><span class="sxs-lookup"><span data-stu-id="f6327-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="f6327-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6327-109">PARAMETERS</span></span>

### <span data-ttu-id="f6327-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6327-110">-DefaultProfile</span></span>
<span data-ttu-id="f6327-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6327-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6327-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f6327-112">-Location</span></span>
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

### <span data-ttu-id="f6327-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="f6327-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="f6327-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6327-114">-ResourceGroupName</span></span>
<span data-ttu-id="f6327-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6327-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6327-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6327-116">CommonParameters</span></span>
<span data-ttu-id="f6327-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6327-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6327-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6327-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6327-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6327-119">INPUTS</span></span>

### <span data-ttu-id="f6327-120">Brak</span><span class="sxs-lookup"><span data-stu-id="f6327-120">None</span></span>

## <span data-ttu-id="f6327-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6327-121">OUTPUTS</span></span>

### <span data-ttu-id="f6327-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6327-122">System.Boolean</span></span>

## <span data-ttu-id="f6327-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6327-123">NOTES</span></span>

## <span data-ttu-id="f6327-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6327-124">RELATED LINKS</span></span>
