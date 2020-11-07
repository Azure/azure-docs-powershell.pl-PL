---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 9d1694cdde3edd94112fc5b1960fd870b842d6e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717514"
---
# <span data-ttu-id="fcc07-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fcc07-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="fcc07-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fcc07-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc07-103">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="fcc07-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc07-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fcc07-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcc07-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fcc07-105">DESCRIPTION</span></span>
<span data-ttu-id="fcc07-106">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="fcc07-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="fcc07-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fcc07-107">EXAMPLES</span></span>

### <span data-ttu-id="fcc07-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fcc07-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="fcc07-109">Aktualizowanie partnera zarządzającego nowym</span><span class="sxs-lookup"><span data-stu-id="fcc07-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="fcc07-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fcc07-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc07-111">-DefaultProfile</span></span>
<span data-ttu-id="fcc07-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fcc07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcc07-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="fcc07-113">-PartnerId</span></span>
<span data-ttu-id="fcc07-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="fcc07-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="fcc07-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fcc07-115">-Confirm</span></span>
<span data-ttu-id="fcc07-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcc07-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc07-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc07-117">-WhatIf</span></span>
<span data-ttu-id="fcc07-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcc07-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc07-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fcc07-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc07-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc07-120">CommonParameters</span></span>
<span data-ttu-id="fcc07-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcc07-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc07-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc07-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc07-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fcc07-123">INPUTS</span></span>

### <span data-ttu-id="fcc07-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fcc07-124">None</span></span>

## <span data-ttu-id="fcc07-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fcc07-125">OUTPUTS</span></span>

### <span data-ttu-id="fcc07-126">Microsoft. Azure. Commands. resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fcc07-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="fcc07-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fcc07-127">NOTES</span></span>

## <span data-ttu-id="fcc07-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fcc07-128">RELATED LINKS</span></span>

[<span data-ttu-id="fcc07-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fcc07-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="fcc07-130">Nowe — AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fcc07-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="fcc07-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fcc07-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
