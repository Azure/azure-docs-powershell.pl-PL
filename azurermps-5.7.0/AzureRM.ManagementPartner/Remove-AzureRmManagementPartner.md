---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 703c38d02ef6a6a339c58c861961cd2ad92ecb7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548983"
---
# <span data-ttu-id="aec13-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="aec13-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="aec13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aec13-102">SYNOPSIS</span></span>
<span data-ttu-id="aec13-103">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="aec13-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aec13-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec13-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aec13-105">DESCRIPTION</span></span>
<span data-ttu-id="aec13-106">Usuń identyfikator sieci partnera firmy Microsoft (MPN) dla bieżącego uwierzytelnionego użytkownika lub usługi.</span><span class="sxs-lookup"><span data-stu-id="aec13-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="aec13-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aec13-107">EXAMPLES</span></span>

### <span data-ttu-id="aec13-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aec13-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="aec13-109">Usuń partnera zarządzania</span><span class="sxs-lookup"><span data-stu-id="aec13-109">Remove management partner</span></span> 

## <span data-ttu-id="aec13-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aec13-110">PARAMETERS</span></span>

### <span data-ttu-id="aec13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec13-111">-DefaultProfile</span></span>
<span data-ttu-id="aec13-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aec13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aec13-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="aec13-113">-PartnerId</span></span>
<span data-ttu-id="aec13-114">Identyfikator partnera zarządzania to numer 6-cyfrowy</span><span class="sxs-lookup"><span data-stu-id="aec13-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="aec13-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aec13-115">-PassThru</span></span>
<span data-ttu-id="aec13-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aec13-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aec13-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aec13-117">-Confirm</span></span>
<span data-ttu-id="aec13-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec13-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec13-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec13-119">-WhatIf</span></span>
<span data-ttu-id="aec13-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec13-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec13-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aec13-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec13-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec13-122">CommonParameters</span></span>
<span data-ttu-id="aec13-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec13-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec13-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec13-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec13-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aec13-125">INPUTS</span></span>

### <span data-ttu-id="aec13-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aec13-126">None</span></span>

## <span data-ttu-id="aec13-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aec13-127">OUTPUTS</span></span>

### <span data-ttu-id="aec13-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="aec13-128">System.Object</span></span>

## <span data-ttu-id="aec13-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aec13-129">NOTES</span></span>

## <span data-ttu-id="aec13-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aec13-130">RELATED LINKS</span></span>

[<span data-ttu-id="aec13-131">Nowe — AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="aec13-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="aec13-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="aec13-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="aec13-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="aec13-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
