---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553575"
---
# <span data-ttu-id="36344-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="36344-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="36344-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36344-102">SYNOPSIS</span></span>
<span data-ttu-id="36344-103">Pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="36344-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36344-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36344-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36344-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36344-105">DESCRIPTION</span></span>
<span data-ttu-id="36344-106">Polecenie cmdlet **Get-AzureRmLogProfile** pobiera profil dziennika.</span><span class="sxs-lookup"><span data-stu-id="36344-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="36344-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36344-107">EXAMPLES</span></span>

## <span data-ttu-id="36344-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36344-108">PARAMETERS</span></span>

### <span data-ttu-id="36344-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36344-109">-DefaultProfile</span></span>
<span data-ttu-id="36344-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="36344-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36344-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36344-111">-Name</span></span>
<span data-ttu-id="36344-112">Określa nazwę profilu dziennika, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="36344-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="36344-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36344-113">CommonParameters</span></span>
<span data-ttu-id="36344-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36344-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36344-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36344-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36344-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36344-116">INPUTS</span></span>

### <span data-ttu-id="36344-117">System. String</span><span class="sxs-lookup"><span data-stu-id="36344-117">System.String</span></span>

## <span data-ttu-id="36344-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36344-118">OUTPUTS</span></span>

### <span data-ttu-id="36344-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="36344-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="36344-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36344-120">NOTES</span></span>

## <span data-ttu-id="36344-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36344-121">RELATED LINKS</span></span>

[<span data-ttu-id="36344-122">Dodaj-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="36344-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="36344-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="36344-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


