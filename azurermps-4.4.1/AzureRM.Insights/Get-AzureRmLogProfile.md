---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: 2964b95dcaba44ba57d354951eb5ccfb4ea9ef6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718200"
---
# <span data-ttu-id="c805e-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c805e-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="c805e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c805e-102">SYNOPSIS</span></span>
<span data-ttu-id="c805e-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="c805e-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c805e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c805e-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c805e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c805e-105">DESCRIPTION</span></span>
<span data-ttu-id="c805e-106">Polecenie cmdlet **Get-AzureRmLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="c805e-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="c805e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c805e-107">EXAMPLES</span></span>

## <span data-ttu-id="c805e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c805e-108">PARAMETERS</span></span>

### <span data-ttu-id="c805e-109">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c805e-109">-Name</span></span>
<span data-ttu-id="c805e-110">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="c805e-110">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="c805e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c805e-111">-DefaultProfile</span></span>
<span data-ttu-id="c805e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c805e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c805e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c805e-113">CommonParameters</span></span>
<span data-ttu-id="c805e-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c805e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c805e-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c805e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c805e-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c805e-116">INPUTS</span></span>

## <span data-ttu-id="c805e-117">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c805e-117">OUTPUTS</span></span>

### <span data-ttu-id="c805e-118">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="c805e-118">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="c805e-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c805e-119">NOTES</span></span>

## <span data-ttu-id="c805e-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c805e-120">RELATED LINKS</span></span>

[<span data-ttu-id="c805e-121">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c805e-121">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="c805e-122">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c805e-122">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


