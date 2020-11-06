---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544812"
---
# <span data-ttu-id="eec57-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="eec57-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="eec57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eec57-102">SYNOPSIS</span></span>
<span data-ttu-id="eec57-103">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eec57-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eec57-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eec57-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec57-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eec57-105">DESCRIPTION</span></span>
<span data-ttu-id="eec57-106">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eec57-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="eec57-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eec57-107">EXAMPLES</span></span>

### <span data-ttu-id="eec57-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eec57-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="eec57-109">Umożliwia zaktualizowanie kontaktu z zabezpieczeniami dla subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eec57-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="eec57-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eec57-110">PARAMETERS</span></span>

### <span data-ttu-id="eec57-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="eec57-111">-AlertAdmin</span></span>
<span data-ttu-id="eec57-112">Alerty dla administratorów.</span><span class="sxs-lookup"><span data-stu-id="eec57-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec57-113">-DefaultProfile</span></span>
<span data-ttu-id="eec57-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eec57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec57-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="eec57-115">-Email</span></span>
<span data-ttu-id="eec57-116">Wysłać.</span><span class="sxs-lookup"><span data-stu-id="eec57-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec57-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eec57-117">-Name</span></span>
<span data-ttu-id="eec57-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="eec57-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec57-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="eec57-119">-NotifyOnAlert</span></span>
<span data-ttu-id="eec57-120">Powiadomienia o alertach.</span><span class="sxs-lookup"><span data-stu-id="eec57-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec57-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="eec57-121">-Phone</span></span>
<span data-ttu-id="eec57-122">Służb.</span><span class="sxs-lookup"><span data-stu-id="eec57-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec57-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eec57-123">-Confirm</span></span>
<span data-ttu-id="eec57-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec57-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec57-125">-WhatIf</span></span>
<span data-ttu-id="eec57-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eec57-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eec57-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eec57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec57-128">CommonParameters</span></span>
<span data-ttu-id="eec57-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec57-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec57-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec57-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eec57-131">INPUTS</span></span>

### <span data-ttu-id="eec57-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eec57-132">System.String</span></span>

## <span data-ttu-id="eec57-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eec57-133">OUTPUTS</span></span>

### <span data-ttu-id="eec57-134">Microsoft. Azure. Commands. Security. models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="eec57-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="eec57-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eec57-135">NOTES</span></span>

## <span data-ttu-id="eec57-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eec57-136">RELATED LINKS</span></span>
