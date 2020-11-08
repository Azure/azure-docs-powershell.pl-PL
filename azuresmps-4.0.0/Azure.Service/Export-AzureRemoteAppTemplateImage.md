---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054647"
---
# <span data-ttu-id="8c4d6-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="8c4d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4d6-103">Eksportuje obraz szablonu jednej kolekcji funkcji Azure RemoteApp do określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="8c4d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c4d6-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4d6-106">Polecenie cmdlet **Export-AzureRemoteAppTemplateImage** Eksportuje obraz szablonu jednej kolekcji funkcji Azure RemoteApp do określonego konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="8c4d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="8c4d6-108">Przykład 1. Eksportowanie obrazu szablonu na konto usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="8c4d6-109">To polecenie eksportuje obraz szablonu o nazwie contoso do kontenera o nazwie ContainerName na określonym koncie usługi Azure Storage, korzystając z nazwy AccountName i Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="8c4d6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c4d6-110">PARAMETERS</span></span>

### <span data-ttu-id="8c4d6-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8c4d6-111">-CollectionName</span></span>
<span data-ttu-id="8c4d6-112">Określa nazwę źródłowej kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d6-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="8c4d6-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="8c4d6-114">Określa nazwę kontenera na docelowym koncie usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d6-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8c4d6-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="8c4d6-116">Określa klucz konta docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d6-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c4d6-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="8c4d6-118">Określa nazwę konta docelowego usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4d6-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="8c4d6-120">Wskazuje, że polecenie cmdlet zastępuje istniejący obraz szablonu.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="8c4d6-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c4d6-121">-Profile</span></span>
<span data-ttu-id="8c4d6-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c4d6-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c4d6-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c4d6-124">-Confirm</span></span>
<span data-ttu-id="8c4d6-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4d6-126">-WhatIf</span></span>
<span data-ttu-id="8c4d6-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4d6-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4d6-129">CommonParameters</span></span>
<span data-ttu-id="8c4d6-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4d6-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4d6-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c4d6-132">INPUTS</span></span>

## <span data-ttu-id="8c4d6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c4d6-133">OUTPUTS</span></span>

## <span data-ttu-id="8c4d6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c4d6-134">NOTES</span></span>

## <span data-ttu-id="8c4d6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c4d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="8c4d6-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8c4d6-137">Nowe — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8c4d6-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="8c4d6-139">Zmień nazwę — AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="8c4d6-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


