---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718024"
---
# <span data-ttu-id="1728f-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="1728f-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="1728f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1728f-102">SYNOPSIS</span></span>
<span data-ttu-id="1728f-103">Uzyskaj członków grupy.</span><span class="sxs-lookup"><span data-stu-id="1728f-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1728f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1728f-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1728f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1728f-105">DESCRIPTION</span></span>
<span data-ttu-id="1728f-106">Uzyskaj członków grupy.</span><span class="sxs-lookup"><span data-stu-id="1728f-106">Get a group members.</span></span>

## <span data-ttu-id="1728f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1728f-107">EXAMPLES</span></span>

### <span data-ttu-id="1728f-108">Filtrowanie członków grupy przy użyciu identyfikatora obiektu grupy</span><span class="sxs-lookup"><span data-stu-id="1728f-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="1728f-109">Pobiera członków grupy o identyfikatorze 85F89C90-780E-4AA6-9F4F-6F268D322EEE</span><span class="sxs-lookup"><span data-stu-id="1728f-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="1728f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1728f-110">PARAMETERS</span></span>

### <span data-ttu-id="1728f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1728f-111">-DefaultProfile</span></span>
<span data-ttu-id="1728f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1728f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1728f-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="1728f-113">-GroupObjectId</span></span>
<span data-ttu-id="1728f-114">Identyfikator obiektu grupy.</span><span class="sxs-lookup"><span data-stu-id="1728f-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1728f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1728f-115">CommonParameters</span></span>
<span data-ttu-id="1728f-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1728f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1728f-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1728f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1728f-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1728f-118">INPUTS</span></span>

### <span data-ttu-id="1728f-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1728f-119">None</span></span>
<span data-ttu-id="1728f-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1728f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1728f-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1728f-121">OUTPUTS</span></span>

### <span data-ttu-id="1728f-122">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADObject]</span><span class="sxs-lookup"><span data-stu-id="1728f-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="1728f-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1728f-123">NOTES</span></span>

## <span data-ttu-id="1728f-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1728f-124">RELATED LINKS</span></span>

[<span data-ttu-id="1728f-125">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1728f-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="1728f-126">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1728f-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

