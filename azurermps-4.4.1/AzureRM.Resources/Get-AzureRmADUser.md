---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527317"
---
# <span data-ttu-id="081eb-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="081eb-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="081eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="081eb-102">SYNOPSIS</span></span>
<span data-ttu-id="081eb-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="081eb-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="081eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="081eb-104">SYNTAX</span></span>

### <span data-ttu-id="081eb-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="081eb-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081eb-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="081eb-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081eb-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="081eb-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081eb-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="081eb-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="081eb-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="081eb-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081eb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="081eb-110">DESCRIPTION</span></span>
<span data-ttu-id="081eb-111">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="081eb-111">Filters active directory users.</span></span>

## <span data-ttu-id="081eb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="081eb-112">EXAMPLES</span></span>

### <span data-ttu-id="081eb-113">--------------------------Filtruje użytkowników przy użyciu głównej nazwy użytkownika--------------------------</span><span class="sxs-lookup"><span data-stu-id="081eb-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="081eb-114">Pobiera użytkownika foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="081eb-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="081eb-115">--------------------------Filtruje użytkowników przy użyciu ciągu wyszukiwania--------------------------</span><span class="sxs-lookup"><span data-stu-id="081eb-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="081eb-116">Umożliwia filtrowanie wszystkich użytkowników usługi AD, którzy mają Janusza, w nazwie wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="081eb-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="081eb-117">--------------------------Listy użytkowników usługi AD--------------------------</span><span class="sxs-lookup"><span data-stu-id="081eb-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="081eb-118">Pobiera wszystkich użytkowników usługi AD</span><span class="sxs-lookup"><span data-stu-id="081eb-118">Gets all AD users</span></span>

## <span data-ttu-id="081eb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="081eb-119">PARAMETERS</span></span>

### <span data-ttu-id="081eb-120">-Mail</span><span class="sxs-lookup"><span data-stu-id="081eb-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081eb-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="081eb-121">-ObjectId</span></span>
<span data-ttu-id="081eb-122">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="081eb-122">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081eb-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="081eb-123">-SearchString</span></span>
<span data-ttu-id="081eb-124">Nazwa wyświetlana użytkownika</span><span class="sxs-lookup"><span data-stu-id="081eb-124">The user display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081eb-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="081eb-125">-UserPrincipalName</span></span>
<span data-ttu-id="081eb-126">UPN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="081eb-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="081eb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081eb-127">-DefaultProfile</span></span>
<span data-ttu-id="081eb-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="081eb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="081eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081eb-129">CommonParameters</span></span>
<span data-ttu-id="081eb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081eb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081eb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081eb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="081eb-132">INPUTS</span></span>

## <span data-ttu-id="081eb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="081eb-133">OUTPUTS</span></span>

### <span data-ttu-id="081eb-134">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="081eb-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="081eb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="081eb-135">NOTES</span></span>

## <span data-ttu-id="081eb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="081eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="081eb-137">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="081eb-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="081eb-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="081eb-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="081eb-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="081eb-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

