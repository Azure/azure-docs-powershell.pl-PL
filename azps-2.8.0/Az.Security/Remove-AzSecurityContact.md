---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: eac99fc2395408f2e140b3369a87e75928006f21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871660"
---
# <span data-ttu-id="69803-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="69803-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="69803-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69803-102">SYNOPSIS</span></span>
<span data-ttu-id="69803-103">Usuwa kontakt z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="69803-103">Deletes a security contact.</span></span>

## <span data-ttu-id="69803-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69803-104">SYNTAX</span></span>

### <span data-ttu-id="69803-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69803-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69803-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="69803-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69803-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="69803-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69803-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69803-108">DESCRIPTION</span></span>
<span data-ttu-id="69803-109">Usuwa kontakt z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="69803-109">Deletes a security contact.</span></span>

## <span data-ttu-id="69803-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69803-110">EXAMPLES</span></span>

### <span data-ttu-id="69803-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69803-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="69803-112">Usuwa kontakt z zabezpieczeniami "default1"</span><span class="sxs-lookup"><span data-stu-id="69803-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="69803-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69803-113">PARAMETERS</span></span>

### <span data-ttu-id="69803-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69803-114">-DefaultProfile</span></span>
<span data-ttu-id="69803-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69803-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69803-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69803-116">-InputObject</span></span>
<span data-ttu-id="69803-117">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="69803-117">Input Object.</span></span>

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

### <span data-ttu-id="69803-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69803-118">-Name</span></span>
<span data-ttu-id="69803-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="69803-119">Resource name.</span></span>

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

### <span data-ttu-id="69803-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69803-120">-PassThru</span></span>
<span data-ttu-id="69803-121">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="69803-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="69803-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69803-122">-ResourceId</span></span>
<span data-ttu-id="69803-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="69803-123">Resource ID.</span></span>

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

### <span data-ttu-id="69803-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69803-124">-Confirm</span></span>
<span data-ttu-id="69803-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69803-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69803-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69803-126">-WhatIf</span></span>
<span data-ttu-id="69803-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69803-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69803-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69803-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69803-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69803-129">CommonParameters</span></span>
<span data-ttu-id="69803-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69803-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69803-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69803-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69803-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69803-132">INPUTS</span></span>

### <span data-ttu-id="69803-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69803-133">System.String</span></span>

### <span data-ttu-id="69803-134">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="69803-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="69803-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69803-135">OUTPUTS</span></span>

### <span data-ttu-id="69803-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69803-136">System.Boolean</span></span>

## <span data-ttu-id="69803-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69803-137">NOTES</span></span>

## <span data-ttu-id="69803-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69803-138">RELATED LINKS</span></span>
