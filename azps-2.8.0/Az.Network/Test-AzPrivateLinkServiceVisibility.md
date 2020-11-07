---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872051"
---
# <span data-ttu-id="a837c-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="a837c-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="a837c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a837c-102">SYNOPSIS</span></span>
<span data-ttu-id="a837c-103">**Test — AzPrivateLinkServiceVisibility** sprawdza, czy usługa linku prywatnego jest widoczna do bieżącego użytku.</span><span class="sxs-lookup"><span data-stu-id="a837c-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="a837c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a837c-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a837c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a837c-105">DESCRIPTION</span></span>
<span data-ttu-id="a837c-106">Sprawdzanie, czy usługa linku prywatnego jest widoczna do użytku bieżącego.</span><span class="sxs-lookup"><span data-stu-id="a837c-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="a837c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a837c-107">EXAMPLES</span></span>

### <span data-ttu-id="a837c-108">Przykład 1: Sprawdź, czy contoso.cloudapp.azure.com jest dostępny do użycia.</span><span class="sxs-lookup"><span data-stu-id="a837c-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="a837c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a837c-109">PARAMETERS</span></span>

### <span data-ttu-id="a837c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a837c-110">-DefaultProfile</span></span>
<span data-ttu-id="a837c-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a837c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a837c-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a837c-112">-Location</span></span>
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

### <span data-ttu-id="a837c-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="a837c-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="a837c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a837c-114">-ResourceGroupName</span></span>
<span data-ttu-id="a837c-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a837c-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a837c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a837c-116">CommonParameters</span></span>
<span data-ttu-id="a837c-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a837c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a837c-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a837c-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a837c-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a837c-119">INPUTS</span></span>

### <span data-ttu-id="a837c-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a837c-120">None</span></span>

## <span data-ttu-id="a837c-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a837c-121">OUTPUTS</span></span>

### <span data-ttu-id="a837c-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a837c-122">System.Boolean</span></span>

## <span data-ttu-id="a837c-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a837c-123">NOTES</span></span>

## <span data-ttu-id="a837c-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a837c-124">RELATED LINKS</span></span>
