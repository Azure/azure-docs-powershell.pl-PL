---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550224"
---
# <span data-ttu-id="9f8e4-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="9f8e4-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="9f8e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8e4-103">Usuwa kontakt z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f8e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f8e4-104">SYNTAX</span></span>

### <span data-ttu-id="9f8e4-105">SubscriptionLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9f8e4-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8e4-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9f8e4-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8e4-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f8e4-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f8e4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9f8e4-108">DESCRIPTION</span></span>
<span data-ttu-id="9f8e4-109">Usuwa kontakt z zabezpieczeniami.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-109">Deletes a security contact.</span></span>

## <span data-ttu-id="9f8e4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f8e4-110">EXAMPLES</span></span>

### <span data-ttu-id="9f8e4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9f8e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="9f8e4-112">Usuwa kontakt z zabezpieczeniami "default1"</span><span class="sxs-lookup"><span data-stu-id="9f8e4-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="9f8e4-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f8e4-113">PARAMETERS</span></span>

### <span data-ttu-id="9f8e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8e4-114">-DefaultProfile</span></span>
<span data-ttu-id="9f8e4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8e4-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9f8e4-116">-InputObject</span></span>
<span data-ttu-id="9f8e4-117">Obiekt wejściowy.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9f8e4-118">-Name</span></span>
<span data-ttu-id="9f8e4-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f8e4-120">-PassThru</span></span>
<span data-ttu-id="9f8e4-121">Zwraca, czy operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9f8e4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f8e4-122">-ResourceId</span></span>
<span data-ttu-id="9f8e4-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f8e4-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f8e4-124">-Confirm</span></span>
<span data-ttu-id="9f8e4-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f8e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f8e4-126">-WhatIf</span></span>
<span data-ttu-id="9f8e4-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f8e4-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f8e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8e4-129">CommonParameters</span></span>
<span data-ttu-id="9f8e4-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f8e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8e4-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8e4-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f8e4-132">INPUTS</span></span>

### <span data-ttu-id="9f8e4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f8e4-133">System.String</span></span>
<span data-ttu-id="9f8e4-134">Microsoft. Azure. polecenia. Security. cmdlets. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="9f8e4-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="9f8e4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f8e4-135">OUTPUTS</span></span>

### <span data-ttu-id="9f8e4-136">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="9f8e4-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="9f8e4-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f8e4-137">NOTES</span></span>

## <span data-ttu-id="9f8e4-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f8e4-138">RELATED LINKS</span></span>
