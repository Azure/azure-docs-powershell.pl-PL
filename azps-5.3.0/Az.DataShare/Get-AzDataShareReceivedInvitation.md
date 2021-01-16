---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377470"
---
# <span data-ttu-id="bd5fb-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="bd5fb-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="bd5fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5fb-103">Pobiera informacje na temat zaproszeń dla użytkowników.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="bd5fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd5fb-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd5fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd5fb-105">DESCRIPTION</span></span>
<span data-ttu-id="bd5fb-106">Polecenie cmdlet **Get-AzDataShareReceivedInvitation** udostępnia informacje na temat wszystkich zaproszeń, które klient posiada receieved.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="bd5fb-107">Jeśli podasz lokalizację lub identyfikator zaproszenia, to polecenie cmdlet zawiera informacje o zaproszeniu w określonej lokalizacji lub o identyfikatorze zaproszenia. W przeciwnym razie zawiera listę zaproszeń wysłanych do konsumenta.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="bd5fb-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd5fb-108">EXAMPLES</span></span>

### <span data-ttu-id="bd5fb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd5fb-109">Example 1</span></span>
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

<span data-ttu-id="bd5fb-110">Ten sposób komunikacji zapewnia informacje na temat zaproszeń dla użytkowników.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="bd5fb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd5fb-111">PARAMETERS</span></span>

### <span data-ttu-id="bd5fb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5fb-112">-DefaultProfile</span></span>
<span data-ttu-id="bd5fb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd5fb-114">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="bd5fb-114">-InvitationId</span></span>
<span data-ttu-id="bd5fb-115">Identyfikator zaproszenia na usługę Azure datashare.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="bd5fb-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bd5fb-116">-Location</span></span>
<span data-ttu-id="bd5fb-117">Lokalizacja zaproszenia do udostępniania danych w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="bd5fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5fb-118">CommonParameters</span></span>
<span data-ttu-id="bd5fb-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd5fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5fb-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd5fb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5fb-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd5fb-121">INPUTS</span></span>

### <span data-ttu-id="bd5fb-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bd5fb-122">None</span></span>

## <span data-ttu-id="bd5fb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd5fb-123">OUTPUTS</span></span>

### <span data-ttu-id="bd5fb-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="bd5fb-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="bd5fb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd5fb-125">NOTES</span></span>

## <span data-ttu-id="bd5fb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd5fb-126">RELATED LINKS</span></span>
