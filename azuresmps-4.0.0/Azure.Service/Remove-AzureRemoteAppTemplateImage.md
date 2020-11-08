---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055115"
---
# <span data-ttu-id="92172-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="92172-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="92172-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92172-102">SYNOPSIS</span></span>
<span data-ttu-id="92172-103">Usuwa obraz szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="92172-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="92172-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92172-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92172-105">Opis</span><span class="sxs-lookup"><span data-stu-id="92172-105">DESCRIPTION</span></span>
<span data-ttu-id="92172-106">Polecenie cmdlet **Remove-AzureRemoteAppTemplateImage** usuwa obraz szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="92172-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="92172-107">Obraz szablonu można usunąć tylko wtedy, gdy nie jest połączony z żadną kolekcją Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="92172-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="92172-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92172-108">EXAMPLES</span></span>

### <span data-ttu-id="92172-109">Przykład 1: Usuwanie obrazu szablonu</span><span class="sxs-lookup"><span data-stu-id="92172-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="92172-110">To polecenie usuwa obrazek szablonu o nazwie ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="92172-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="92172-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92172-111">PARAMETERS</span></span>

### <span data-ttu-id="92172-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="92172-112">-ImageName</span></span>
<span data-ttu-id="92172-113">Określa nazwę obrazu szablonu funkcji RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="92172-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92172-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="92172-114">-Profile</span></span>
<span data-ttu-id="92172-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92172-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="92172-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="92172-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="92172-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92172-117">-Confirm</span></span>
<span data-ttu-id="92172-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92172-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92172-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92172-119">-WhatIf</span></span>
<span data-ttu-id="92172-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92172-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92172-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92172-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92172-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92172-122">CommonParameters</span></span>
<span data-ttu-id="92172-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92172-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92172-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92172-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92172-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92172-125">INPUTS</span></span>

## <span data-ttu-id="92172-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92172-126">OUTPUTS</span></span>

## <span data-ttu-id="92172-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92172-127">NOTES</span></span>

## <span data-ttu-id="92172-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92172-128">RELATED LINKS</span></span>

[<span data-ttu-id="92172-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="92172-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="92172-130">Nowe — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="92172-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="92172-131">Zmień nazwę — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="92172-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


