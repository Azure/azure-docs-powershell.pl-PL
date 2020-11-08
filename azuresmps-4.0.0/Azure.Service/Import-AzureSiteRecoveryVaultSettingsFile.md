---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055226"
---
# <span data-ttu-id="df6fc-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="df6fc-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="df6fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="df6fc-103">Importuje plik ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="df6fc-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="df6fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df6fc-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df6fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="df6fc-106">Polecenie cmdlet **Import-AzureSiteRecoveryVaultSettingsFile** umożliwia zaimportowanie pliku ustawień magazynu odzyskiwania witryny platformy Azure w celu ustawienia kontekstu magazynu dla kolejnych operacji odzyskiwania witryny w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="df6fc-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="df6fc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="df6fc-108">Przykład 1: Importowanie pliku ustawień magazynu</span><span class="sxs-lookup"><span data-stu-id="df6fc-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="df6fc-109">To polecenie powoduje zaimportowanie pliku ustawień magazynu w określonej ścieżce.</span><span class="sxs-lookup"><span data-stu-id="df6fc-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="df6fc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="df6fc-111">-Path</span><span class="sxs-lookup"><span data-stu-id="df6fc-111">-Path</span></span>
<span data-ttu-id="df6fc-112">Określa ścieżkę pliku ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="df6fc-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="df6fc-113">Ten plik można pobrać z portalu magazynu odzyskiwania witryny i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="df6fc-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6fc-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="df6fc-114">-Profile</span></span>
<span data-ttu-id="df6fc-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df6fc-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df6fc-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="df6fc-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df6fc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6fc-117">CommonParameters</span></span>
<span data-ttu-id="df6fc-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df6fc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df6fc-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df6fc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6fc-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df6fc-120">INPUTS</span></span>

## <span data-ttu-id="df6fc-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df6fc-121">OUTPUTS</span></span>

## <span data-ttu-id="df6fc-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df6fc-122">NOTES</span></span>

## <span data-ttu-id="df6fc-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df6fc-123">RELATED LINKS</span></span>

[<span data-ttu-id="df6fc-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="df6fc-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="df6fc-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="df6fc-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


