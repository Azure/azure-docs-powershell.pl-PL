---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 735ea22547183b8047a3a32d0a147b428b39f630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551632"
---
# <span data-ttu-id="28fb3-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28fb3-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="28fb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="28fb3-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28fb3-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28fb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28fb3-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28fb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="28fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="28fb3-106">Usuwa użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="28fb3-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="28fb3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28fb3-107">EXAMPLES</span></span>

### <span data-ttu-id="28fb3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="28fb3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="28fb3-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="28fb3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="28fb3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28fb3-110">PARAMETERS</span></span>

### <span data-ttu-id="28fb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28fb3-111">-DefaultProfile</span></span>
<span data-ttu-id="28fb3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="28fb3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28fb3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="28fb3-113">-Force</span></span>
<span data-ttu-id="28fb3-114">Jeśli ta osoba jest określona, nie prosi o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28fb3-114">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28fb3-115">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="28fb3-115">-UPNOrObjectId</span></span>
<span data-ttu-id="28fb3-116">Główna nazwa użytkownika lub identyfikator obiektu (objectId) użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="28fb3-116">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28fb3-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28fb3-117">-Confirm</span></span>
<span data-ttu-id="28fb3-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28fb3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28fb3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28fb3-119">-WhatIf</span></span>
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

### <span data-ttu-id="28fb3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28fb3-120">CommonParameters</span></span>
<span data-ttu-id="28fb3-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28fb3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28fb3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28fb3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28fb3-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28fb3-123">INPUTS</span></span>

### <span data-ttu-id="28fb3-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="28fb3-124">None</span></span>
<span data-ttu-id="28fb3-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="28fb3-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28fb3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28fb3-126">OUTPUTS</span></span>

## <span data-ttu-id="28fb3-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28fb3-127">NOTES</span></span>

## <span data-ttu-id="28fb3-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28fb3-128">RELATED LINKS</span></span>

[<span data-ttu-id="28fb3-129">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28fb3-129">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="28fb3-130">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28fb3-130">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="28fb3-131">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="28fb3-131">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

