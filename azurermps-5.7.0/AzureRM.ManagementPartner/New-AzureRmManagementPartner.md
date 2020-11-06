---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549695"
---
# <span data-ttu-id="a0a1a-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a0a1a-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="a0a1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a1a-103">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0a1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0a1a-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0a1a-106">Kojarzy identyfikator sieci partnera firmy Microsoft (MPN) z bieżącym użytkownikiem uwierzytelnionym lub usługą.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a0a1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="a0a1a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0a1a-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="a0a1a-109">Dodawanie partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="a0a1a-109">Add a management partner</span></span> 

## <span data-ttu-id="a0a1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="a0a1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a1a-111">-DefaultProfile</span></span>
<span data-ttu-id="a0a1a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a1a-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="a0a1a-113">-PartnerId</span></span>
<span data-ttu-id="a0a1a-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="a0a1a-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a1a-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0a1a-115">-Confirm</span></span>
<span data-ttu-id="a0a1a-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a1a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a1a-117">-WhatIf</span></span>
<span data-ttu-id="a0a1a-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a1a-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0a1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a1a-120">CommonParameters</span></span>
<span data-ttu-id="a0a1a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0a1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a1a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0a1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a1a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0a1a-123">INPUTS</span></span>

### <span data-ttu-id="a0a1a-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a0a1a-124">None</span></span>

## <span data-ttu-id="a0a1a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0a1a-125">OUTPUTS</span></span>

### <span data-ttu-id="a0a1a-126">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a0a1a-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="a0a1a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0a1a-127">NOTES</span></span>

## <span data-ttu-id="a0a1a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0a1a-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0a1a-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a0a1a-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="a0a1a-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a0a1a-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="a0a1a-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a0a1a-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
