---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 20d258cdd99da4e76fcf8394ebbe1aadd54f2fb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704891"
---
# <span data-ttu-id="b21ef-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b21ef-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="b21ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b21ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b21ef-103">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="b21ef-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b21ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b21ef-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b21ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b21ef-106">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="b21ef-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b21ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b21ef-107">EXAMPLES</span></span>

### <span data-ttu-id="b21ef-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b21ef-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b21ef-109">Aktualizowanie partnera zarządzającego nowym</span><span class="sxs-lookup"><span data-stu-id="b21ef-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="b21ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b21ef-110">PARAMETERS</span></span>

### <span data-ttu-id="b21ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21ef-111">-DefaultProfile</span></span>
<span data-ttu-id="b21ef-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b21ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b21ef-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b21ef-113">-PartnerId</span></span>
<span data-ttu-id="b21ef-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="b21ef-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ef-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b21ef-115">-Confirm</span></span>
<span data-ttu-id="b21ef-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b21ef-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ef-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21ef-117">-WhatIf</span></span>
<span data-ttu-id="b21ef-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b21ef-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21ef-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b21ef-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21ef-120">CommonParameters</span></span>
<span data-ttu-id="b21ef-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b21ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21ef-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21ef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21ef-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b21ef-123">INPUTS</span></span>

### <span data-ttu-id="b21ef-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b21ef-124">None</span></span>

## <span data-ttu-id="b21ef-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b21ef-125">OUTPUTS</span></span>

### <span data-ttu-id="b21ef-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b21ef-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b21ef-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b21ef-127">NOTES</span></span>

## <span data-ttu-id="b21ef-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b21ef-128">RELATED LINKS</span></span>

[<span data-ttu-id="b21ef-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b21ef-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="b21ef-130">Nowe — AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b21ef-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b21ef-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b21ef-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)