---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718716"
---
# <span data-ttu-id="4bd7a-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4bd7a-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="4bd7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd7a-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bd7a-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd7a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4bd7a-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd7a-106">Usuwa użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="4bd7a-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="4bd7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bd7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4bd7a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4bd7a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4bd7a-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="4bd7a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4bd7a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bd7a-110">PARAMETERS</span></span>

### <span data-ttu-id="4bd7a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4bd7a-111">-Force</span></span>
<span data-ttu-id="4bd7a-112">Jeśli ta osoba jest określona, nie prosi o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

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

### <span data-ttu-id="4bd7a-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="4bd7a-113">-UPNOrObjectId</span></span>
<span data-ttu-id="4bd7a-114">Główna nazwa użytkownika lub identyfikator obiektu (objectId) użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-114">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7a-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4bd7a-115">-Confirm</span></span>
<span data-ttu-id="4bd7a-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bd7a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd7a-117">-WhatIf</span></span>
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

### <span data-ttu-id="4bd7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd7a-118">-DefaultProfile</span></span>
<span data-ttu-id="4bd7a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd7a-120">CommonParameters</span></span>
<span data-ttu-id="4bd7a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd7a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd7a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bd7a-123">INPUTS</span></span>

## <span data-ttu-id="4bd7a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bd7a-124">OUTPUTS</span></span>

## <span data-ttu-id="4bd7a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bd7a-125">NOTES</span></span>

## <span data-ttu-id="4bd7a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bd7a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4bd7a-127">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4bd7a-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="4bd7a-128">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4bd7a-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="4bd7a-129">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4bd7a-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

