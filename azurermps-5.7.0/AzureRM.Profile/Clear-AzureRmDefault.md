---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525038"
---
# <span data-ttu-id="32ba8-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="32ba8-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="32ba8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="32ba8-103">Czyści ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="32ba8-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32ba8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32ba8-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ba8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="32ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="32ba8-106">Polecenie cmdlet Clear-AzureRmDefault usuwa ustawienia domyślne ustawiane przez użytkownika w zależności od parametrów przełącznika określonych przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="32ba8-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="32ba8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="32ba8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32ba8-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="32ba8-109">To polecenie usuwa wszystkie ustawienia domyślne ustawione przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="32ba8-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="32ba8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="32ba8-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="32ba8-111">To polecenie usuwa domyślną grupę zasobów ustawioną przez użytkownika w bieżącym kontekście.</span><span class="sxs-lookup"><span data-stu-id="32ba8-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="32ba8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32ba8-112">PARAMETERS</span></span>

### <span data-ttu-id="32ba8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ba8-113">-DefaultProfile</span></span>
<span data-ttu-id="32ba8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32ba8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32ba8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="32ba8-115">-Force</span></span>
<span data-ttu-id="32ba8-116">Usuwanie wszystkich ustawień domyślnych, jeśli nie określono wartości domyślnej</span><span class="sxs-lookup"><span data-stu-id="32ba8-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="32ba8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32ba8-117">-PassThru</span></span>
<span data-ttu-id="32ba8-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="32ba8-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32ba8-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="32ba8-119">-ResourceGroup</span></span>
<span data-ttu-id="32ba8-120">Wyczyść domyślną grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="32ba8-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ba8-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32ba8-121">-Confirm</span></span>
<span data-ttu-id="32ba8-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32ba8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ba8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ba8-123">-WhatIf</span></span>
<span data-ttu-id="32ba8-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32ba8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ba8-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32ba8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ba8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ba8-126">CommonParameters</span></span>
<span data-ttu-id="32ba8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ba8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ba8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ba8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ba8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32ba8-129">INPUTS</span></span>

### <span data-ttu-id="32ba8-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32ba8-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32ba8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32ba8-131">OUTPUTS</span></span>

### <span data-ttu-id="32ba8-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="32ba8-132">System.Object</span></span>

## <span data-ttu-id="32ba8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32ba8-133">NOTES</span></span>

## <span data-ttu-id="32ba8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32ba8-134">RELATED LINKS</span></span>

