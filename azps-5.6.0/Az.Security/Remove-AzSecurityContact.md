---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992419"
---
# <span data-ttu-id="37aa0-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="37aa0-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="37aa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="37aa0-103">Usuwa kontakt zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="37aa0-103">Deletes a security contact.</span></span>

## <span data-ttu-id="37aa0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37aa0-104">SYNTAX</span></span>

### <span data-ttu-id="37aa0-105">SubscriptionLevelResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="37aa0-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37aa0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="37aa0-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37aa0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="37aa0-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37aa0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="37aa0-108">DESCRIPTION</span></span>
<span data-ttu-id="37aa0-109">Usuwa kontakt zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="37aa0-109">Deletes a security contact.</span></span>

## <span data-ttu-id="37aa0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37aa0-110">EXAMPLES</span></span>

### <span data-ttu-id="37aa0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37aa0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="37aa0-112">Usuwa kontakt zabezpieczeń "default1"</span><span class="sxs-lookup"><span data-stu-id="37aa0-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="37aa0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37aa0-113">PARAMETERS</span></span>

### <span data-ttu-id="37aa0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37aa0-114">-DefaultProfile</span></span>
<span data-ttu-id="37aa0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37aa0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37aa0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37aa0-116">-InputObject</span></span>
<span data-ttu-id="37aa0-117">Obiekt Input.</span><span class="sxs-lookup"><span data-stu-id="37aa0-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37aa0-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37aa0-118">-Name</span></span>
<span data-ttu-id="37aa0-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="37aa0-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37aa0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37aa0-120">-PassThru</span></span>
<span data-ttu-id="37aa0-121">Sprawdź, czy operacja się powiedzie.</span><span class="sxs-lookup"><span data-stu-id="37aa0-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="37aa0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37aa0-122">-ResourceId</span></span>
<span data-ttu-id="37aa0-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="37aa0-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37aa0-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37aa0-124">-Confirm</span></span>
<span data-ttu-id="37aa0-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37aa0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37aa0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37aa0-126">-WhatIf</span></span>
<span data-ttu-id="37aa0-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37aa0-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37aa0-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37aa0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37aa0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37aa0-129">CommonParameters</span></span>
<span data-ttu-id="37aa0-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37aa0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37aa0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37aa0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37aa0-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37aa0-132">INPUTS</span></span>

### <span data-ttu-id="37aa0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="37aa0-133">System.String</span></span>

### <span data-ttu-id="37aa0-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="37aa0-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="37aa0-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37aa0-135">OUTPUTS</span></span>

### <span data-ttu-id="37aa0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37aa0-136">System.Boolean</span></span>

## <span data-ttu-id="37aa0-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37aa0-137">NOTES</span></span>

## <span data-ttu-id="37aa0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37aa0-138">RELATED LINKS</span></span>
