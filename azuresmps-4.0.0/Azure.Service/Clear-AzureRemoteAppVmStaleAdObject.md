---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054669"
---
# <span data-ttu-id="4c040-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="4c040-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="4c040-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c040-102">SYNOPSIS</span></span>
<span data-ttu-id="4c040-103">Usuwa obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi Azure RemoteApp, które już nie istnieją.</span><span class="sxs-lookup"><span data-stu-id="4c040-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="4c040-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c040-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c040-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c040-105">DESCRIPTION</span></span>
<span data-ttu-id="4c040-106">Polecenie cmdlet **Clear-AzureRemoteAppVmStaleAdObject** usuwa obiekty w usłudze Azure Active Directory skojarzone z maszynami wirtualnymi usługi Azure RemoteApp, które już nie istnieją.</span><span class="sxs-lookup"><span data-stu-id="4c040-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="4c040-107">Musisz użyć poświadczeń, które mają uprawnienia do usuwania obiektów usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4c040-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="4c040-108">W przypadku określenia parametru Common *verbose* to polecenie cmdlet wyświetla nazwę każdego usuniętego obiektu.</span><span class="sxs-lookup"><span data-stu-id="4c040-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="4c040-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c040-109">EXAMPLES</span></span>

### <span data-ttu-id="4c040-110">Przykład 1. Wyczyść stare obiekty dla kolekcji</span><span class="sxs-lookup"><span data-stu-id="4c040-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="4c040-111">Po pierwszym poleceniu zostanie wyświetlony monit o podanie nazwy użytkownika i hasła przy użyciu funkcji **Uzyskaj-Credential**.</span><span class="sxs-lookup"><span data-stu-id="4c040-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="4c040-112">Polecenie zapisuje wyniki w zmiennej $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="4c040-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="4c040-113">Drugie polecenie czyści stare obiekty dla kolekcji o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="4c040-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="4c040-114">Polecenie korzysta z poświadczeń przechowywanych w zmiennej $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="4c040-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="4c040-115">Aby wykonanie polecenia powiodło się, te poświadczenia muszą mieć odpowiednie prawa.</span><span class="sxs-lookup"><span data-stu-id="4c040-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="4c040-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c040-116">PARAMETERS</span></span>

### <span data-ttu-id="4c040-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="4c040-117">-CollectionName</span></span>
<span data-ttu-id="4c040-118">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="4c040-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="4c040-119">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="4c040-119">-Credential</span></span>
<span data-ttu-id="4c040-120">Określa poświadczenie, które ma uprawnienia do wykonania tej akcji.</span><span class="sxs-lookup"><span data-stu-id="4c040-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="4c040-121">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="4c040-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="4c040-122">Jeśli nie podano tego parametru, to polecenie cmdlet użyje bieżących poświadczeń użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4c040-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="4c040-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="4c040-123">-Profile</span></span>
<span data-ttu-id="4c040-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c040-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c040-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4c040-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c040-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c040-126">-Confirm</span></span>
<span data-ttu-id="4c040-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c040-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c040-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c040-128">-WhatIf</span></span>
<span data-ttu-id="4c040-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c040-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c040-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c040-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c040-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c040-131">CommonParameters</span></span>
<span data-ttu-id="4c040-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c040-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c040-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c040-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c040-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c040-134">INPUTS</span></span>

## <span data-ttu-id="4c040-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c040-135">OUTPUTS</span></span>

## <span data-ttu-id="4c040-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c040-136">NOTES</span></span>

## <span data-ttu-id="4c040-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c040-137">RELATED LINKS</span></span>

[<span data-ttu-id="4c040-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="4c040-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


