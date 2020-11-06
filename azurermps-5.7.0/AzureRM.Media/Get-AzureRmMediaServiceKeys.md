---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545644"
---
# <span data-ttu-id="6d52f-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6d52f-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="6d52f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d52f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d52f-103">Pobiera kluczowe informacje dotyczące uzyskiwania dostępu do punktu końcowego usługi w usłudze multimediów skojarzonego z usługą Media.</span><span class="sxs-lookup"><span data-stu-id="6d52f-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d52f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d52f-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d52f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6d52f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d52f-106">Polecenie cmdlet **Get-AzureRmMediaServiceKeys** pobiera informacje kluczowe o uzyskiwaniu dostępu do punktu końcowego przenoszenia stanu (pozostałej) skojarzonego z usługą Azure Media.</span><span class="sxs-lookup"><span data-stu-id="6d52f-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="6d52f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d52f-107">EXAMPLES</span></span>

### <span data-ttu-id="6d52f-108">Przykład 1: uzyskiwanie najważniejszych informacji dotyczących uzyskiwania dostępu do usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="6d52f-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="6d52f-109">To polecenie pobiera kluczowe informacje dotyczące uzyskiwania dostępu do usługi multimedialnej o nazwie MediaService001 należącej do grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="6d52f-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="6d52f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d52f-110">PARAMETERS</span></span>

### <span data-ttu-id="6d52f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d52f-111">-AccountName</span></span>
<span data-ttu-id="6d52f-112">Określa nazwę usługi multimedialnej, z której to polecenie cmdlet pobiera klucze usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="6d52f-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d52f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d52f-113">-DefaultProfile</span></span>
<span data-ttu-id="6d52f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6d52f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d52f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d52f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d52f-116">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="6d52f-116">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d52f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d52f-117">CommonParameters</span></span>
<span data-ttu-id="6d52f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d52f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d52f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d52f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d52f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d52f-120">INPUTS</span></span>

### <span data-ttu-id="6d52f-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d52f-121">None</span></span>
<span data-ttu-id="6d52f-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6d52f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d52f-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d52f-123">OUTPUTS</span></span>

### <span data-ttu-id="6d52f-124">Microsoft. Azure. Commands. Media. models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6d52f-124">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="6d52f-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d52f-125">NOTES</span></span>

## <span data-ttu-id="6d52f-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d52f-126">RELATED LINKS</span></span>

[<span data-ttu-id="6d52f-127">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6d52f-127">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


