---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: db87797573d3f6c06b52aa072773c9af1a1be1fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329504"
---
# <span data-ttu-id="0fee6-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0fee6-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="0fee6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0fee6-102">SYNOPSIS</span></span>
<span data-ttu-id="0fee6-103">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="0fee6-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0fee6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0fee6-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fee6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0fee6-105">DESCRIPTION</span></span>
<span data-ttu-id="0fee6-106">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="0fee6-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0fee6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0fee6-107">EXAMPLES</span></span>

### <span data-ttu-id="0fee6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0fee6-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="0fee6-109">Usuń partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="0fee6-109">Remove management partner</span></span>

## <span data-ttu-id="0fee6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0fee6-110">PARAMETERS</span></span>

### <span data-ttu-id="0fee6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fee6-111">-DefaultProfile</span></span>
<span data-ttu-id="0fee6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0fee6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fee6-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0fee6-113">-PartnerId</span></span>
<span data-ttu-id="0fee6-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="0fee6-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0fee6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fee6-115">-PassThru</span></span>
<span data-ttu-id="0fee6-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0fee6-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fee6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0fee6-117">-Confirm</span></span>
<span data-ttu-id="0fee6-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fee6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fee6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fee6-119">-WhatIf</span></span>
<span data-ttu-id="0fee6-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fee6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fee6-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0fee6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fee6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fee6-122">CommonParameters</span></span>
<span data-ttu-id="0fee6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fee6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fee6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fee6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fee6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0fee6-125">INPUTS</span></span>

### <span data-ttu-id="0fee6-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0fee6-126">None</span></span>

## <span data-ttu-id="0fee6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0fee6-127">OUTPUTS</span></span>

### <span data-ttu-id="0fee6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fee6-128">System.Boolean</span></span>

## <span data-ttu-id="0fee6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0fee6-129">NOTES</span></span>

## <span data-ttu-id="0fee6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0fee6-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fee6-131">Nowe — AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0fee6-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="0fee6-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0fee6-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="0fee6-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0fee6-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)