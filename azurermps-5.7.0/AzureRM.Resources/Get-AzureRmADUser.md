---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717706"
---
# <span data-ttu-id="4e0b7-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e0b7-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="4e0b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0b7-103">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e0b7-104">SYNTAX</span></span>

### <span data-ttu-id="4e0b7-105">EmptyParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e0b7-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e0b7-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e0b7-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e0b7-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e0b7-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e0b7-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e0b7-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e0b7-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e0b7-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e0b7-110">Opis</span><span class="sxs-lookup"><span data-stu-id="4e0b7-110">DESCRIPTION</span></span>
<span data-ttu-id="4e0b7-111">Umożliwia filtrowanie użytkowników usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-111">Filters active directory users.</span></span>

## <span data-ttu-id="4e0b7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e0b7-112">EXAMPLES</span></span>

### <span data-ttu-id="4e0b7-113">Filtruje użytkowników przy użyciu głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="4e0b7-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="4e0b7-114">Pobiera użytkownika foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="4e0b7-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="4e0b7-115">Filtruje użytkowników przy użyciu ciągu wyszukiwania</span><span class="sxs-lookup"><span data-stu-id="4e0b7-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="4e0b7-116">Umożliwia filtrowanie wszystkich użytkowników usługi AD, którzy mają Janusza, w nazwie wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="4e0b7-117">Lista użytkowników usługi AD</span><span class="sxs-lookup"><span data-stu-id="4e0b7-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="4e0b7-118">Pobiera wszystkich użytkowników usługi AD</span><span class="sxs-lookup"><span data-stu-id="4e0b7-118">Gets all AD users</span></span>

## <span data-ttu-id="4e0b7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e0b7-119">PARAMETERS</span></span>

### <span data-ttu-id="4e0b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0b7-120">-DefaultProfile</span></span>
<span data-ttu-id="4e0b7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4e0b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e0b7-122">-Mail</span><span class="sxs-lookup"><span data-stu-id="4e0b7-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0b7-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4e0b7-123">-ObjectId</span></span>
<span data-ttu-id="4e0b7-124">Identyfikator obiektu użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0b7-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="4e0b7-125">-SearchString</span></span>
<span data-ttu-id="4e0b7-126">Nazwa wyświetlana użytkownika</span><span class="sxs-lookup"><span data-stu-id="4e0b7-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0b7-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4e0b7-127">-UserPrincipalName</span></span>
<span data-ttu-id="4e0b7-128">UPN użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0b7-129">CommonParameters</span></span>
<span data-ttu-id="4e0b7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0b7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0b7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0b7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e0b7-132">INPUTS</span></span>

### <span data-ttu-id="4e0b7-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4e0b7-133">None</span></span>
<span data-ttu-id="4e0b7-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4e0b7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e0b7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e0b7-135">OUTPUTS</span></span>

### <span data-ttu-id="4e0b7-136">System. Collections. Generic. list "1 [Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="4e0b7-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="4e0b7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e0b7-137">NOTES</span></span>

## <span data-ttu-id="4e0b7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e0b7-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e0b7-139">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e0b7-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="4e0b7-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e0b7-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="4e0b7-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4e0b7-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

