---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 18cd37f1e24851720299a647a30323f9379bea6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050135"
---
# <span data-ttu-id="8fdaf-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="8fdaf-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="8fdaf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8fdaf-103">Pobiera informacje na temat zaproszeń dla użytkowników.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="8fdaf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fdaf-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fdaf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8fdaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8fdaf-106">Polecenie cmdlet **Get-AzDataShareReceivedInvitation** udostępnia informacje na temat wszystkich zaproszeń, które klient posiada receieved.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="8fdaf-107">Jeśli podasz lokalizację lub identyfikator zaproszenia, to polecenie cmdlet zawiera informacje o zaproszeniu w określonej lokalizacji lub o identyfikatorze zaproszenia. W przeciwnym razie zawiera listę zaproszeń wysłanych do konsumenta.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="8fdaf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fdaf-108">EXAMPLES</span></span>

### <span data-ttu-id="8fdaf-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fdaf-109">Example 1</span></span>
```
PS C:\> Get-AzDataShareReceivedInvitation -location "westus"

DataSetCount      : 3
InvitationId      : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus  : Pending
Location          : westus
RespondedAt       :
Sender            : adsprovider@microsoft.com
SenderCompanyName : ADS Test
SentAt            : 7/8/2019 10:47:10 PM
ShareName         : AdsShare
Description       : Some description
Terms             : Some terms of use
Id                : /providers/Microsoft.DataShare/consumerInvitations/167e06ff-567f-4bc7-be0c-645a6de710f3
Name              : AdsInvitation
Type              : Microsoft.DataShare/consumerInvitations
```

<span data-ttu-id="8fdaf-110">Ten sposób komunikacji zapewnia informacje na temat zaproszeń dla użytkowników.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="8fdaf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fdaf-111">PARAMETERS</span></span>

### <span data-ttu-id="8fdaf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fdaf-112">-DefaultProfile</span></span>
<span data-ttu-id="8fdaf-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fdaf-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="8fdaf-114">-InvitationId</span></span>
<span data-ttu-id="8fdaf-115">Identyfikator zaproszenia na usługę Azure datashare.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-115">Azure dataShare invitation id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdaf-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8fdaf-116">-Location</span></span>
<span data-ttu-id="8fdaf-117">Lokalizacja zaproszenia do udostępniania danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-117">Azure data share invitation location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fdaf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fdaf-118">CommonParameters</span></span>
<span data-ttu-id="8fdaf-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fdaf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fdaf-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fdaf-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fdaf-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fdaf-121">INPUTS</span></span>

### <span data-ttu-id="8fdaf-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8fdaf-122">None</span></span>

## <span data-ttu-id="8fdaf-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fdaf-123">OUTPUTS</span></span>

### <span data-ttu-id="8fdaf-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8fdaf-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8fdaf-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fdaf-125">NOTES</span></span>

## <span data-ttu-id="8fdaf-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fdaf-126">RELATED LINKS</span></span>
