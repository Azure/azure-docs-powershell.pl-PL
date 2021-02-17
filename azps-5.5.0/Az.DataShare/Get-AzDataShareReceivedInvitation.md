---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharereceivedinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareReceivedInvitation.md
ms.openlocfilehash: 939b50f6725497bb28ea333f13c04c6281f34611
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198075"
---
# <span data-ttu-id="7dba9-101">Get-AzDataShareReceivedInvitation</span><span class="sxs-lookup"><span data-stu-id="7dba9-101">Get-AzDataShareReceivedInvitation</span></span>

## <span data-ttu-id="7dba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dba9-102">SYNOPSIS</span></span>
<span data-ttu-id="7dba9-103">Pobiera informacje o zaproszeniach dla klientów.</span><span class="sxs-lookup"><span data-stu-id="7dba9-103">Gets information about consumer invitations.</span></span>

## <span data-ttu-id="7dba9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7dba9-104">SYNTAX</span></span>

```
Get-AzDataShareReceivedInvitation [-Location <String>] [-InvitationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dba9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7dba9-105">DESCRIPTION</span></span>
<span data-ttu-id="7dba9-106">Polecenie **cmdlet Get-AzDataShareReceivedInvitation** zawiera informacje o wszystkich zaproszeniach, które zostały ponownie wysłane przez klienta.</span><span class="sxs-lookup"><span data-stu-id="7dba9-106">The **Get-AzDataShareReceivedInvitation** cmdlet provides information about all the invitations that the consumer has receieved.</span></span> <span data-ttu-id="7dba9-107">Jeśli po podaję lokalizację lub identyfikator zaproszenia, to polecenie cmdlet będzie zawierało informacje o zaproszeniu w konkretnej lokalizacji lub o identyfikatorze zaproszenia. W przeciwnym razie zostanie wyświetlona lista zaproszeń wysłanych do klienta.</span><span class="sxs-lookup"><span data-stu-id="7dba9-107">If you provide location or invitation id, this cmdlet provides information about invitation in particular location or having invitation id. Otherwise, it provides a list of invitations sent to the consumer.</span></span>

## <span data-ttu-id="7dba9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7dba9-108">EXAMPLES</span></span>

### <span data-ttu-id="7dba9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7dba9-109">Example 1</span></span>
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

<span data-ttu-id="7dba9-110">Ten commant zawiera informacje o zaproszeniach dla klientów.</span><span class="sxs-lookup"><span data-stu-id="7dba9-110">This commant provides information about consumer invitations.</span></span>

## <span data-ttu-id="7dba9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dba9-111">PARAMETERS</span></span>

### <span data-ttu-id="7dba9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dba9-112">-DefaultProfile</span></span>
<span data-ttu-id="7dba9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dba9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dba9-114">- InvitationId</span><span class="sxs-lookup"><span data-stu-id="7dba9-114">-InvitationId</span></span>
<span data-ttu-id="7dba9-115">Identyfikator zaproszenia usługi Azure dataShare.</span><span class="sxs-lookup"><span data-stu-id="7dba9-115">Azure dataShare invitation id.</span></span>

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

### <span data-ttu-id="7dba9-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7dba9-116">-Location</span></span>
<span data-ttu-id="7dba9-117">Lokalizacja zaproszeń udostępniania danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7dba9-117">Azure data share invitation location.</span></span>

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

### <span data-ttu-id="7dba9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dba9-118">CommonParameters</span></span>
<span data-ttu-id="7dba9-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dba9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dba9-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dba9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dba9-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dba9-121">INPUTS</span></span>

### <span data-ttu-id="7dba9-122">Brak</span><span class="sxs-lookup"><span data-stu-id="7dba9-122">None</span></span>

## <span data-ttu-id="7dba9-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dba9-123">OUTPUTS</span></span>

### <span data-ttu-id="7dba9-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="7dba9-124">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="7dba9-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7dba9-125">NOTES</span></span>

## <span data-ttu-id="7dba9-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dba9-126">RELATED LINKS</span></span>
