---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894613"
---
# <span data-ttu-id="fbc6b-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fbc6b-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="fbc6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbc6b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc6b-103">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="fbc6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbc6b-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbc6b-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc6b-106">Umożliwia zaktualizowanie identyfikatora sieci partnera firmy Microsoft (MPN) bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="fbc6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbc6b-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc6b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fbc6b-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="fbc6b-109">Aktualizowanie partnera zarządzającego nowym</span><span class="sxs-lookup"><span data-stu-id="fbc6b-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="fbc6b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbc6b-110">PARAMETERS</span></span>

### <span data-ttu-id="fbc6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc6b-111">-DefaultProfile</span></span>
<span data-ttu-id="fbc6b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbc6b-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="fbc6b-113">-PartnerId</span></span>
<span data-ttu-id="fbc6b-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="fbc6b-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="fbc6b-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbc6b-115">-Confirm</span></span>
<span data-ttu-id="fbc6b-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc6b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc6b-117">-WhatIf</span></span>
<span data-ttu-id="fbc6b-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc6b-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc6b-120">CommonParameters</span></span>
<span data-ttu-id="fbc6b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc6b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc6b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc6b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbc6b-123">INPUTS</span></span>

### <span data-ttu-id="fbc6b-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fbc6b-124">None</span></span>

## <span data-ttu-id="fbc6b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbc6b-125">OUTPUTS</span></span>

### <span data-ttu-id="fbc6b-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fbc6b-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="fbc6b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbc6b-127">NOTES</span></span>

## <span data-ttu-id="fbc6b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbc6b-128">RELATED LINKS</span></span>

[<span data-ttu-id="fbc6b-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fbc6b-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="fbc6b-130">Nowe — AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fbc6b-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="fbc6b-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="fbc6b-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)