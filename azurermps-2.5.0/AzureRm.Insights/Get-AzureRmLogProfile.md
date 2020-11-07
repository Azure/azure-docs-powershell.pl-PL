---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 29ff6159501bccd73947e25a65ec765a49b8859c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897454"
---
# <span data-ttu-id="dd31d-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="dd31d-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="dd31d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd31d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd31d-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="dd31d-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd31d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd31d-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd31d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd31d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd31d-106">Polecenie cmdlet **Get-AzureRmLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="dd31d-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="dd31d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd31d-107">EXAMPLES</span></span>

## <span data-ttu-id="dd31d-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd31d-108">PARAMETERS</span></span>

### <span data-ttu-id="dd31d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd31d-109">-DefaultProfile</span></span>
<span data-ttu-id="dd31d-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd31d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd31d-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd31d-111">-Name</span></span>
<span data-ttu-id="dd31d-112">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="dd31d-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="dd31d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd31d-113">CommonParameters</span></span>
<span data-ttu-id="dd31d-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd31d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd31d-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd31d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd31d-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd31d-116">INPUTS</span></span>

### <span data-ttu-id="dd31d-117">System. String</span><span class="sxs-lookup"><span data-stu-id="dd31d-117">System.String</span></span>

## <span data-ttu-id="dd31d-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd31d-118">OUTPUTS</span></span>

### <span data-ttu-id="dd31d-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="dd31d-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="dd31d-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd31d-120">NOTES</span></span>

## <span data-ttu-id="dd31d-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd31d-121">RELATED LINKS</span></span>

[<span data-ttu-id="dd31d-122">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="dd31d-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="dd31d-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="dd31d-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


