---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546744"
---
# <span data-ttu-id="94032-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="94032-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="94032-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94032-102">SYNOPSIS</span></span>
<span data-ttu-id="94032-103">Pobiera identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="94032-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94032-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94032-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94032-105">Opis</span><span class="sxs-lookup"><span data-stu-id="94032-105">DESCRIPTION</span></span>
<span data-ttu-id="94032-106">Pobiera identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="94032-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="94032-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94032-107">EXAMPLES</span></span>

### <span data-ttu-id="94032-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94032-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="94032-109">Uzyskiwanie identyfikatora bieżącego partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="94032-109">Get the current management partner id</span></span>

### <span data-ttu-id="94032-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94032-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="94032-111">Uzyskaj bieżący identyfikator partnera zarządzania przy użyciu identyfikatora partnera, jeśli nie jest on zgodny, nie powiedzie się</span><span class="sxs-lookup"><span data-stu-id="94032-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="94032-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94032-112">PARAMETERS</span></span>

### <span data-ttu-id="94032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94032-113">-DefaultProfile</span></span>
<span data-ttu-id="94032-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94032-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94032-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="94032-115">-PartnerId</span></span>
<span data-ttu-id="94032-116">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="94032-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94032-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94032-117">CommonParameters</span></span>
<span data-ttu-id="94032-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94032-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94032-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94032-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94032-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94032-120">INPUTS</span></span>

### <span data-ttu-id="94032-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="94032-121">None</span></span>

## <span data-ttu-id="94032-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94032-122">OUTPUTS</span></span>

### <span data-ttu-id="94032-123">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="94032-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="94032-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94032-124">NOTES</span></span>

## <span data-ttu-id="94032-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94032-125">RELATED LINKS</span></span>

[<span data-ttu-id="94032-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="94032-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="94032-127">Nowe — AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="94032-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="94032-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="94032-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
