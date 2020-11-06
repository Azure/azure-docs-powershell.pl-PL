---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: b96c8717e20395c57e6c9d5d4520327d97dfa174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544296"
---
# <span data-ttu-id="39079-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="39079-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="39079-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39079-102">SYNOPSIS</span></span>
<span data-ttu-id="39079-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="39079-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39079-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39079-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39079-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39079-105">DESCRIPTION</span></span>
<span data-ttu-id="39079-106">Polecenie cmdlet **Get-AzureRmLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="39079-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="39079-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39079-107">EXAMPLES</span></span>

## <span data-ttu-id="39079-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39079-108">PARAMETERS</span></span>

### <span data-ttu-id="39079-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39079-109">-DefaultProfile</span></span>
<span data-ttu-id="39079-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="39079-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39079-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="39079-111">-Name</span></span>
<span data-ttu-id="39079-112">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="39079-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39079-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39079-113">CommonParameters</span></span>
<span data-ttu-id="39079-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39079-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39079-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39079-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39079-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39079-116">INPUTS</span></span>

### <span data-ttu-id="39079-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39079-117">None</span></span>
<span data-ttu-id="39079-118">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="39079-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39079-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39079-119">OUTPUTS</span></span>

### <span data-ttu-id="39079-120">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="39079-120">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="39079-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39079-121">NOTES</span></span>

## <span data-ttu-id="39079-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39079-122">RELATED LINKS</span></span>

[<span data-ttu-id="39079-123">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="39079-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="39079-124">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="39079-124">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


