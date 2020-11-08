---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054596"
---
# <span data-ttu-id="75db4-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="75db4-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="75db4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75db4-102">SYNOPSIS</span></span>
<span data-ttu-id="75db4-103">Pobiera obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.</span><span class="sxs-lookup"><span data-stu-id="75db4-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="75db4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75db4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="75db4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75db4-105">DESCRIPTION</span></span>
<span data-ttu-id="75db4-106">Polecenie cmdlet **Get-AzureRemoteAppVmStaleAdObject** Pobiera obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.</span><span class="sxs-lookup"><span data-stu-id="75db4-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="75db4-107">To polecenie cmdlet spowoduje wyświetlenie nazwy każdego z obiektów, które ma on pobierać.</span><span class="sxs-lookup"><span data-stu-id="75db4-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="75db4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75db4-108">EXAMPLES</span></span>

### <span data-ttu-id="75db4-109">Przykład 1: pobieranie starych obiektów dla kolekcji</span><span class="sxs-lookup"><span data-stu-id="75db4-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="75db4-110">To drugie polecenie pobiera stare obiekty kolekcji o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="75db4-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="75db4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75db4-111">PARAMETERS</span></span>

### <span data-ttu-id="75db4-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="75db4-112">-CollectionName</span></span>
<span data-ttu-id="75db4-113">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75db4-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75db4-114">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="75db4-114">-Credential</span></span>
<span data-ttu-id="75db4-115">Określa poświadczenie, które ma uprawnienia do wykonania tej akcji.</span><span class="sxs-lookup"><span data-stu-id="75db4-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="75db4-116">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="75db4-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="75db4-117">Jeśli nie podano tego parametru, to polecenie cmdlet użyje bieżących poświadczeń użytkownika.</span><span class="sxs-lookup"><span data-stu-id="75db4-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75db4-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="75db4-118">-Profile</span></span>
<span data-ttu-id="75db4-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75db4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75db4-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="75db4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75db4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75db4-121">CommonParameters</span></span>
<span data-ttu-id="75db4-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75db4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75db4-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75db4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75db4-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75db4-124">INPUTS</span></span>

## <span data-ttu-id="75db4-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75db4-125">OUTPUTS</span></span>

### <span data-ttu-id="75db4-126">Ciąg</span><span class="sxs-lookup"><span data-stu-id="75db4-126">String</span></span>

## <span data-ttu-id="75db4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75db4-127">NOTES</span></span>

## <span data-ttu-id="75db4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75db4-128">RELATED LINKS</span></span>

[<span data-ttu-id="75db4-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="75db4-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


